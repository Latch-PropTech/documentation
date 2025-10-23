# Setup Instructions for docs.latch.ooo

This guide walks you through publishing this documentation site to GitHub Pages and configuring your custom subdomain.

## Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the **+** icon in the top right and select **New repository**
3. Configure the repository:
   - **Repository name**: `documentation`
   - **Description**: "User documentation for Latch property management platform"
   - **Visibility**: Choose Public or Private (GitHub Pages works with both)
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)
4. Click **Create repository**

## Step 2: Push Your Local Repository to GitHub

After creating the repository on GitHub, you'll see instructions. Use these commands:

```bash
cd ~/Dev/latch/documentation

# Add the remote (replace YOUR-USERNAME with your GitHub username or org)
git remote add origin git@github.com:YOUR-USERNAME/documentation.git

# Push to GitHub
git branch -M main
git push -u origin main
```

**Example** (if your GitHub org is `latch-app`):
```bash
git remote add origin git@github.com:latch-app/documentation.git
git branch -M main
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. In the left sidebar, click **Pages** (under "Code and automation")
4. Under **Source**:
   - Select **Deploy from a branch**
   - **Branch**: Select `main`
   - **Folder**: Select `/ (root)`
5. Click **Save**

GitHub will start building your site. This takes 1-2 minutes.

Your site will initially be available at: `https://YOUR-USERNAME.github.io/documentation/`

## Step 4: Configure Custom Domain (docs.latch.ooo)

### 4a: Add Custom Domain in GitHub Pages

1. Still in **Settings > Pages**
2. Under **Custom domain**, enter: `docs.latch.ooo`
3. Click **Save**
4. GitHub will create a `CNAME` file in your repository
5. **Wait** before checking "Enforce HTTPS" - we need to set up DNS first

### 4b: Configure DNS Records

You need to add DNS records to your domain registrar (wherever latch.ooo is managed - likely GoDaddy, Cloudflare, Namecheap, etc.).

Add the following DNS records:

#### Option 1: CNAME Record (Recommended)

Add a **CNAME** record:
- **Type**: CNAME
- **Name**: `docs` (or `docs.latch.ooo` depending on your DNS provider)
- **Value**: `YOUR-USERNAME.github.io` (replace with your actual GitHub username/org)
- **TTL**: 3600 (or use default)

**Example**:
```
Type: CNAME
Name: docs
Value: latch-app.github.io
TTL: 3600
```

#### Option 2: A Records (Alternative)

If your DNS provider doesn't support CNAME for subdomains, use A records pointing to GitHub's IP addresses:

Add **four A records**:
- **Type**: A
- **Name**: `docs`
- **Value**: (add these four IPs as separate records)
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- **TTL**: 3600

### 4c: Wait for DNS Propagation

DNS changes can take anywhere from 5 minutes to 48 hours to propagate, though typically it's quite fast (15-30 minutes).

You can check DNS propagation status at: https://www.whatsmydns.net/#CNAME/docs.latch.ooo

### 4d: Enable HTTPS

Once DNS is propagated:

1. Go back to **Settings > Pages** in GitHub
2. Check the box **Enforce HTTPS**
3. Wait a few minutes for the SSL certificate to be issued

## Step 5: Verify Your Site

Visit https://docs.latch.ooo - you should see your documentation homepage!

## Troubleshooting

### "There isn't a GitHub Pages site here"

- **Cause**: DNS hasn't propagated yet, or GitHub Pages hasn't finished building
- **Solution**: Wait 15-30 minutes and try again. Check build status in **Actions** tab on GitHub.

### "Your connection is not private" (SSL error)

- **Cause**: SSL certificate hasn't been issued yet
- **Solution**: Wait up to 20 minutes after DNS propagation for GitHub to issue the certificate.

### "Page not found" after clicking links

- **Cause**: Jekyll hasn't built yet, or there's a configuration error
- **Solution**: Check the **Actions** tab in your GitHub repository for build errors.

### DNS isn't resolving

- **Cause**: Incorrect DNS configuration
- **Solution**:
  1. Verify you added the CNAME or A records correctly
  2. Check DNS with: `dig docs.latch.ooo` or `nslookup docs.latch.ooo`
  3. Make sure there are no conflicting DNS records

## Making Updates

To add or update documentation:

1. Edit files locally in `~/Dev/latch/documentation/`
2. Commit your changes:
   ```bash
   cd ~/Dev/latch/documentation
   git add .
   git commit -m "Update documentation"
   git push
   ```
3. GitHub Pages will automatically rebuild (takes 1-2 minutes)
4. Changes will appear at https://docs.latch.ooo

## Adding New Pages

1. Create a new `.md` file in the root directory
2. Add front matter at the top:
   ```yaml
   ---
   layout: default
   title: Your Page Title
   permalink: /your-page/
   ---

   # Your content here
   ```
3. Optionally, add the page to navigation in `_config.yml` under `header_pages:`
4. Commit and push

## Local Testing

To preview changes locally before pushing:

```bash
cd ~/Dev/latch/documentation

# First time only: install dependencies
bundle install

# Run Jekyll locally
bundle exec jekyll serve

# Open http://localhost:4000 in your browser
```

## Need Help?

- **GitHub Pages Docs**: https://docs.github.com/en/pages
- **Jekyll Docs**: https://jekyllrb.com/docs/
- **Custom Domain Setup**: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

---

## Quick Reference

### Repository Details
- **Local path**: `~/Dev/latch/documentation/`
- **GitHub repo**: `github.com/YOUR-USERNAME/documentation`
- **Live site**: `https://docs.latch.ooo`

### Key Files
- `_config.yml` - Jekyll configuration
- `index.md` - Homepage
- `amenities.md` - Amenities guide
- `assets/images/` - Screenshots and images
- `Gemfile` - Ruby dependencies

### Useful Commands
```bash
# Navigate to documentation
cd ~/Dev/latch/documentation

# Check status
git status

# Push changes
git add .
git commit -m "Your message"
git push

# Test locally
bundle exec jekyll serve
```
