# RPS Compliance Model

Monitoring dashboard and computation engine for DOE Renewable Portfolio Standards compliance of a single electric cooperative.
Static, client-side PWA: no backend. Uploaded workbooks are processed in the browser only.

## Files
- `index.html` – the whole app (formula engine, UI, ANECO-structured workbook template embedded)
- `vendor/` – Chart.js 4.4.1 and JSZip 3.10.1 (bundled; works offline except the optional Inter font)
- `manifest.webmanifest`, `icon.svg`, `sw.js` – PWA install + offline cache
- `render.yaml` – Render static-site blueprint
- optional `bg.jpg` – page background image (shown subtly if present; add it to the repo root)

## Deploy on Render
Push this folder to the repo root (`cotelcotrading/rps-navigator`). Render redeploys automatically (Static Site, Publish Directory `.`).

## Updating
Bump `const V='rps-compliance-model-v2'` in `sw.js` so installed copies refresh.
