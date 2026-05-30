# Alex Crome's Personal Site

A personal portfolio website built with [Hugo](https://gohugo.io/) and the [Terminal](https://github.com/panr/hugo-theme-terminal) theme, deployed to GitHub Pages.

## Prerequisites

- [Hugo Extended](https://gohugo.io/installation/) v0.162.1 or later
- [Go](https://golang.org/dl/) 1.26 or later (for Hugo Modules)

## Local Development

### Preview the website

```bash
# Install Hugo module dependencies
hugo mod tidy

# Start the local development server
hugo server --buildDrafts
```

The site will be available at `http://localhost:1313/`

Changes to content and configuration files will automatically rebuild and refresh in your browser.

### Build for production

```bash
hugo --minify
```

This generates the optimized static site in the `public/` directory.

## Project Structure

```
.
├── content/          # Site content (pages, posts)
├── layouts/          # Custom page templates (empty by default; theme provides defaults)
├── static/           # Static files (copied as-is to public/)
├── hugo.toml         # Site configuration
├── go.mod            # Hugo module dependencies
└── .github/workflows/hugo.yml  # CI/CD workflow for GitHub Pages
```

## Deployment

The site automatically deploys to GitHub Pages when you push to the `master` branch via the `.github/workflows/hugo.yml` workflow.

**Manual repo setup:**
1. In GitHub repo Settings → Pages, set **Source** to "GitHub Actions"

## Theme Configuration

The site uses the [hugo-theme-terminal](https://github.com/panr/hugo-theme-terminal) theme, imported as a Hugo Module (no git submodules).

Theme settings are configured in `hugo.toml` under `[params]` and `[[menu.main]]`.

## License

See LICENSE file (if present).
