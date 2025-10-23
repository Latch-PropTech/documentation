# CLAUDE.md

Guidance for Claude Code when working with Latch documentation.

## Documentation Standards

### Writing Style
- **Concise and practical** - Focus on clear instructions, not marketing fluff
- **No placeholder content** - Only real, useful information
- **Assume basic competence** - Users know how to login; skip obvious steps
- **No contact information** - Remove all "Need Help?" sections and email addresses
- **Screenshot-driven** - Use screenshots to illustrate every key step

### Content Structure
- Start with clear "Overview" and "What You Can Do" sections
- Provide step-by-step instructions with numbered steps
- Include example use cases with real requirements
- Add "Tips and Best Practices" sections
- Include "Troubleshooting" and "FAQ" sections where relevant

## Repository Structure

### File Organization
- Documentation pages: Root directory as `.md` files
- Images: `assets/images/{feature-name}/` (e.g., `assets/images/amenities/`)
- Portal screenshots: Numbered `01-description.png`, `02-description.png`, etc.
- Mobile screenshots: Prefixed with `mobile-01-description.png`, etc.

### Jekyll Configuration
- **Local preview**: `bundle exec jekyll serve --livereload`
- **URL**: Site runs at `http://localhost:4000`
- **Deployment**: Automatic via GitHub Pages to `https://docs.latch.ooo`

## Creating Documentation with Screenshots

### Environment Access
- Portal (staff): `http://localhost:4200` - Login credentials in `CREDENTIALS.md`
- Tenant app: `http://localhost:4201` - Login credentials in `CREDENTIALS.md`
- Mobile viewport: 375x667 for mobile screenshots
- **Ionic framework**: Be careful with scrolling - select proper scroll containers

### Screenshot Guidelines
1. Use Playwright to capture screenshots systematically
2. Navigate through complete workflows
3. Capture every significant screen in the flow
4. Name files descriptively: `{sequence}-{description}.png`
5. Organize by feature in `assets/images/{feature}/`

### Documentation Workflow
1. Capture all portal screenshots first (staff perspective)
2. Capture all mobile app screenshots (tenant perspective)
3. Write documentation with both perspectives
4. Test locally with Jekyll
5. Commit and push to GitHub (auto-deploys to docs.latch.ooo)

## Git Workflow

### Making Changes
```bash
cd ~/Dev/latch/documentation

# Make changes to .md files or assets
# Jekyll auto-reloads if running with --livereload

git add .
git commit -m "Update documentation"
git push
```

### Adding New Pages
1. Create new `.md` file in root directory
2. Add front matter:
   ```yaml
   ---
   layout: default
   title: Page Title
   permalink: /page-url/
   ---
   ```
3. Add to `_config.yml` under `header_pages:` if needed for navigation
4. Create corresponding `assets/images/{feature}/` directory for screenshots
5. Commit and push

## Key Files
- `_config.yml` - Jekyll and site configuration
- `Gemfile` - Ruby dependencies (use `github-pages` gem)
- `index.md` - Homepage
- `_includes/header.html` - Custom header with Latch logo
- `.gitignore` - Excludes `CREDENTIALS.md` and other local files
