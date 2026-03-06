# Underwriting Documentation Portal

Documentation portal for underwriting initiatives, UWWB, shared capabilities, and audit evidence — built with [MkDocs](https://www.mkdocs.org/) and the [Material theme](https://squidfunk.github.io/mkdocs-material/).

## Live Site

The site is published to GitHub Pages at:
**<https://pasingh-msig.github.io/Underwriting-documentation-portal/>**

## Local Preview

**Prerequisites:** Python 3.x

```bash
pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000> in your browser.

## Build

```bash
mkdocs build
```

The static site is generated in the `site/` directory.

## Deployment

Deployment to GitHub Pages happens automatically via GitHub Actions whenever changes are pushed to the `main` branch. The workflow is defined in `.github/workflows/deploy.yml`.

To trigger a manual deployment, go to **Actions → Deploy MkDocs to GitHub Pages → Run workflow**.

### GitHub Pages Configuration

In the repository **Settings → Pages**:
- **Source**: Deploy from a branch
- **Branch**: `gh-pages` / `/ (root)`

The workflow uses `mkdocs gh-deploy` which pushes the built site to the `gh-pages` branch automatically.

## Included

- `mkdocs.yml` — site configuration and navigation
- `docs/` — all documentation source files
  - `docs/index.md` — home page
  - `docs/portfolio-overview.md` — portfolio overview
  - `docs/shared/` — shared standards (glossary, architecture, governance, etc.)
  - `docs/initiatives/` — per-initiative documentation (overview, audit, applications)
  - `docs/doc-templates/` — reusable markdown templates
  - `docs/robots.txt` — crawler exclusion file (deployed to site root)
- `overrides/main.html` — MkDocs Material theme override that injects the `noindex` meta tag
- `requirements.txt` — Python dependencies (`mkdocs`, `mkdocs-material`)
- `.github/workflows/deploy.yml` — GitHub Actions deployment workflow

## Search Engine Indexing Protections

This site is intentionally configured to discourage search engine indexing and crawling.

### What was added

1. **`docs/robots.txt`** — Served at `/robots.txt` on the published site; instructs all compliant crawlers not to index any page:
   ```
   User-agent: *
   Disallow: /
   ```
2. **`overrides/main.html`** — MkDocs Material theme template override that injects the following tag into the `<head>` of every rendered page:
   ```html
   <meta name="robots" content="noindex, nofollow, noarchive">
   ```

### How to verify

- **robots.txt**: Visit `https://pasingh-msig.github.io/Underwriting-documentation-portal/robots.txt` after deployment and confirm the content matches the above.
- **noindex meta tag**: Open any published page, right-click → *View Page Source*, and search for `noindex` in the `<head>` section.

### Limitations

- The repository must remain **public** for GitHub Pages to work. The site content is therefore publicly accessible by anyone with the URL.
- `robots.txt` and the `noindex` directive are advisory — search engines are expected to comply, but non-compliant or malicious bots can ignore them.
- These controls **do not** restrict direct access to the site; they only discourage automated indexing.

