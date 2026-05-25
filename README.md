# Auris site

Static HTML site, 5 pages, ready for GitHub Pages.

## Pages
- `index.html` — Home (entry point)
- `how.html` — How it works
- `features.html` — Features
- `pricing.html` — Pricing
- `privacy.html` — Privacy
- `terms.html` — Terms

## Deploy to GitHub Pages
1. Create a new GitHub repo (e.g. `auris-site`).
2. Drop the contents of this folder into the repo root and push.
3. Repo → **Settings** → **Pages**.
4. **Source**: Deploy from a branch.
5. **Branch**: `main` (or your default), folder `/ (root)`.
6. Save. Your site goes live at `https://<user>.github.io/<repo>/` within a minute.

If you'd rather keep the HTML in a subfolder, move everything into `/docs` and pick `/docs` as the Pages folder instead.

No build step. No dependencies. Open `index.html` locally to preview.
