# Auris UI

Five-page static site for Auris, ready for GitHub Pages.

## Pages
- `index.html` — Home / landing
- `how.html` — How it works
- `features.html` — Features spec sheet
- `privacy.html` — Privacy story
- `pricing.html` — Pricing

## Deploy
Drop the whole folder into a GitHub repo. In **Settings → Pages**, set the source to your default branch root. The site loads at `https://<user>.github.io/<repo>/` and resolves `index.html` automatically.

For a custom domain, add a `CNAME` file in the root with one line (e.g. `auris.talk`) and point your DNS at GitHub Pages.

## Notes
- Single font: Albert Sans (loaded from Google Fonts).
- All pages share the same masthead nav. If you change it on one page, update the others to match.
- No build step. No JavaScript framework. Edit any `.html` file directly.
