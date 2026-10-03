# 2Qua Water Watch — Researcher Dashboard
Static dashboard (Leaflet + Chart.js). No backend.

- `index.html` — page structure · `css/styles.css` — all styling (colors in `:root`) · `js/app.js` — logic
- `data/dashboard_data.json` — exported pipeline data · `data/spatial_maps_png/` + `data/spatial_manifest.json` — map overlays

**Updating data:** replace `dashboard_data.json`, add new PNGs, then regenerate the manifest:
`python -c "import os,json;json.dump(sorted(f for f in os.listdir('data/spatial_maps_png') if f.endswith('.png')),open('data/spatial_manifest.json','w'))"`

**Run locally:** `python -m http.server` then open http://localhost:8000 (opening index.html via file:// blocks data loading).
