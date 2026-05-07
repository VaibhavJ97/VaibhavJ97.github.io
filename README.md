# 🚀 Portfolio Site v5 — Clean Final Version

## ✨ What's in this version

A fully working multi-page CV portfolio with a **live ensemble-based interactive map**, with NO placeholder Google Drive links.

### What was removed in v5
- ❌ All `[Certificate (add link) →]` placeholder buttons
- ❌ All `[Reference (add link) →]` placeholder pills
- ❌ Cert cards no longer link anywhere — they're clean visual badges
- ❌ Note about "click to view on Google Drive" in cert section header

The page is now visually clean — no broken/empty placeholder UI.

---

## 📂 What's still in here (your real CV content)

### Homepage (`index.html`)
- Hero + about (3 paragraphs)
- Skills overview (3 columns) + detailed skills + 3 languages
- **3 work experiences** (IONOS, Hydrosion, KIT) with full bullet points
- **3 education entries** (KIT M.Sc., NIT M.Tech, B.Sc.) with thesis details, scholarships, volunteering listed inline
- **4 internships & research projects** (Birbal Sahni, Oil India, ONGC, Kumaun University)
- **11 certifications** as clean badge cards
- **7 field excursions** as chips
- Contact: only email + GitHub (no phone, no address)

### Live Map (`maps-page/live-explorer.html`) — Ensemble-based
- Loads all 8 CMIP6 GCMs for chosen scenario
- Computes **Mean / P25 / P50 (Median) / P75** per pixel — exactly like your notebook
- 4 stat tabs to switch between statistics
- Germany boundary drawn from public Natural Earth GeoJSON
- Click anywhere → popup shows ALL 4 stats at that point
- Per-model means table in sidebar
- 5 colormap options

### Other pages
- `thesis/index.html` — Research overview with download cards (notebook + GeoTIFFs + GitHub repo)
- `maps-page/index.html` — Maps hub with featured live explorer card

---

## 📁 File structure

```
your-repo/
├── index.html              ← Full CV homepage (CLEAN)
├── assets/
│   └── style.css
├── thesis/
│   └── index.html
├── maps-page/
│   ├── index.html
│   ├── live-explorer.html  ← ⭐ Ensemble live map
│   └── map_*.html          ← 6 placeholder folium slots
├── files/
│   └── Single_BHE_Analysis_GEE_CMIP6_Folium.ipynb
└── data/                   ← Your 16 TIFFs (already on GitHub — keep!)
```

---

## 🚀 Deploy

### Step 1: Clean up GitHub
At https://github.com/VaibhavJ97/VaibhavJ97.github.io, delete:
- Old `index.html`, `files/`, `maps-page/`, `thesis/`, `assets/`

⚠️ **Keep the `data/` folder** — your 16 TIFFs are needed for the live map!

### Step 2: Upload v5
1. Unzip this archive
2. On GitHub: "Add file" → "Upload files"
3. Open the `portfolio-v5` folder, select all (Ctrl+A), drag in
4. Commit
5. Wait 1-2 minutes

### Step 3: Test
- Homepage: https://VaibhavJ97.github.io
- Live map: https://VaibhavJ97.github.io/maps-page/live-explorer.html

The live map takes ~10-30s on first load (fetching 8 TIFFs), then everything is cached and instant.

---

## 💡 Want to add Google Drive links later?

If you change your mind later and want certificate cards to be clickable:
1. In `index.html`, find the certs section: `<!-- ============ CERTIFICATIONS ============ -->`
2. Each cert is a `<div class="cert">...</div>`
3. Change `<div class="cert">` to `<a class="cert" href="YOUR_URL" target="_blank">`
4. Change the closing `</div>` to `</a>`

Just message me when you have the links and I can do it for you in one batch.
