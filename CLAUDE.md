# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Architecture

Single static HTML page — no build step, no framework, no dependencies. Everything
(markup, CSS, layout) lives inline in `index.html`. Served directly by GitHub Pages
(repo is `mv-mt/jessefitzgerald.github.io`) at jessefitzgerald.com (see `CNAME`).

This is the root landing page linking out to the other sites:
- `https://portfolio.jessefitzgerald.com` — photography portfolio (`jf-portfolio` repo)
- `https://blog.jessefitzgerald.com` — blog (`jf-blog` repo)
- `mailto:hello@jessefitzgerald.com`

## Commands

No build/dev server — edit `index.html` directly and preview by opening it in a browser
or with a local static server (e.g. `python3 -m http.server`). Push to `main` to deploy;
GitHub Pages serves the repo directly, no CI step.

## Assets

`favicon.png`, `favicon.svg`, `apple-touch-icon.png`, `logo.svg`, `photo.jpg` are all
committed directly to the repo root (no CDN/R2, unlike `jf-portfolio`).

## Gotchas

- Don't confuse this repo with `jf-portfolio` or `jf-blog` — it only holds the landing
  page, not any gallery or post content.
- A duplicate clone of this repo previously existed nested inside `jf-portfolio/` by
  accident; it's been removed. This (`~/dev/jf-landing`) is the canonical checkout.
