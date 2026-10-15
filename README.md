# RPS Navigator

DOE Renewable Portfolio Standards compliance dashboard and computation engine for Philippine electric cooperatives.
Static, client-side PWA: no backend, no database. Uploaded workbooks are processed in the browser only.

## Files
- `index.html` – the whole app (engine, UI, study data, template v1.0 embedded)
- `vendor/` – Chart.js 4.4.1 and SheetJS 0.18.5 (bundled; app works without CDNs, except the optional Inter web font)
- `manifest.webmanifest`, `icon.svg`, `sw.js` – PWA install + offline cache
- `render.yaml` – Render Blueprint for a static site

## Deploy on Render
1. Push this folder to the root of a GitHub repository.
2. Render dashboard -> New -> Blueprint (or New -> Static Site) -> select the repo.
   Static Site settings: Build Command blank, Publish Directory `.`
3. Open the `https://<name>.onrender.com` URL; use the browser's Install option.

## Updating
Edit `index.html`, then bump `const V='rps-navigator-v1'` in `sw.js` (e.g. `rps-navigator-v2`) so installed copies refresh. Push to `main`.

## Local test
`python3 -m http.server 8080` then open http://localhost:8080
