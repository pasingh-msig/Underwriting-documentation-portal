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

### GitHub Pages Configuration Required

After merging, configure GitHub Pages in the repository settings:

1. Go to **Settings → Pages**
2. Set **Source**: Deploy from a branch
3. Set **Branch**: `gh-pages` / `/ (root)`

The workflow uses `mkdocs gh-deploy` which pushes the built site to the `gh-pages` branch automatically.

## Included

- `mkdocs.yml` — site configuration and navigation
- `docs/` — all documentation source files
  - `docs/index.md` — home page
  - `docs/portfolio-overview.md` — portfolio overview
  - `docs/shared/` — shared standards (glossary, architecture, governance, etc.)
  - `docs/initiatives/` — per-initiative documentation (overview, audit, applications)
  - `docs/doc-templates/` — reusable markdown templates
- `requirements.txt` — Python dependencies (`mkdocs`, `mkdocs-material`)
- `.github/workflows/deploy.yml` — GitHub Actions deployment workflow

