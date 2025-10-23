# Latch Documentation

This repository contains user-facing documentation for the Latch property management platform.

## 🌐 Live Site

The documentation is published at: [https://docs.latch.ooo](https://docs.latch.ooo)

## 📚 Contents

- **Amenities Guide**: Complete guide for setting up and managing bookable amenities

## 🛠️ Local Development

This site uses Jekyll and GitHub Pages.

### Running locally:

```bash
# Install Jekyll (if not already installed)
gem install bundler jekyll

# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve
```

Then visit `http://localhost:4000`

## 📝 Contributing

1. Create a new markdown file in the root or in a subdirectory
2. Add front matter at the top:
   ```yaml
   ---
   layout: default
   title: Your Page Title
   ---
   ```
3. Write your content in Markdown
4. Commit and push to main branch
5. GitHub Pages will automatically rebuild and deploy

## 🎨 Structure

- `_config.yml` - Jekyll configuration
- `index.md` - Homepage
- `amenities.md` - Amenities feature guide
- `assets/` - Images, CSS, and other static files
- `_layouts/` - HTML templates (optional custom layouts)

## 🚀 Deployment

This site is automatically deployed via GitHub Pages when changes are pushed to the `main` branch.

