# 67Runner Official Website

This repository is a small GitHub Pages site for 67Runner. It uses GitHub's
built-in Jekyll build when the `main` branch is published through Pages.

## GitHub Pages setup

In the public repository, configure:

- **Settings → Pages → Source:** Deploy from a branch
- **Branch:** `main`
- **Folder:** `/ (root)`

GitHub will process `_config.yml`, the layouts, includes, and Markdown pages
when the branch is updated. Do not commit a generated `_site/` directory.

If a custom domain or `username.github.io` site is used instead, change
`baseurl` in `_config.yml` to an empty value:

```yaml
baseurl: ""
```

The generated legal pages are available at:

- `/privacy/`
- `/terms/`
- `/contact/`
- `/impressum/`
