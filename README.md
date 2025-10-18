# Anmol's Blog + Portfolio (Jekyll on GitHub Pages)

This is a lightweight, fully GitHub Pages–compatible Jekyll site with:
- Blog posts for long-form writing
- A **Daily** collection for short logs/journaling
- A **Projects** page for your portfolio
- SEO + RSS out of the box (`jekyll-seo-tag`, `jekyll-feed`)

## Quick Start (No local install)
1. Create a new public repo on GitHub (e.g., `anmol-blog`).
2. Upload everything from this folder to the repo root.
3. Go to **Settings → Pages → Build and deployment**: choose **GitHub Actions** or **Deploy from a branch** (main branch, root).
4. Wait for the site to build, then open the URL GitHub gives you.

## Optional: Run locally
- Install Ruby (3.x) and Bundler.
- In the project folder:
  ```bash
  bundle install
  bundle exec jekyll serve
  ```
- Open http://127.0.0.1:4000

## Edit navigation
The top navigation is controlled by `header_pages` in `_config.yml`.
