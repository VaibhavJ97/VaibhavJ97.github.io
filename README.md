# 🚀 Portfolio Site v4 (FINAL) — Ensemble-based live map

## ✨ The big change in this version

**The live map now matches your Jupyter notebook exactly.** Instead of showing one TIFF at a time, it loads ALL 8 climate models and computes ensemble statistics per pixel — Mean, P25, P50 (Median), P75 — exactly like cells 37-38 of your notebook (`np.nanmean` and `np.nanpercentile` across the model stack).

### How the new live map works

1. **Choose a scenario** (SSP 2-4.5 or SSP 5-8.5)
2. The browser loads all 8 GCM TIFFs for that scenario
3. For each pixel, it stacks the 8 values and computes **Mean, P25, P50, P75**
4. Click any of the 4 statistic tabs — the map redraws with that statistic
5. The sidebar shows ensemble-wide aggregates + per-model means
6. Click anywhere on Germany → popup shows **all 4 stats** at that point

This is **exactly the analysis from your notebook**, now live in the browser.

### Germany boundary
✅ Added — drawn over the map using public Natural Earth GeoJSON

---

## 📋 Other things in v4

### Removed (per your request)
- ❌ Both CV PDFs
- ❌ Master thesis PDF download
- ❌ GEE Analysis PDF download
- ❌ Phone number
- ❌ Address

### Homepage
Full CV-style page with:
- Hero + about (3 paragraphs)
- Skills overview + detailed skills + languages
- **3 jobs** (IONOS, Hydrosion, KIT) with full bullet points + Reference link placeholders
- **3 degrees** (KIT M.Sc., NIT M.Tech, B.Sc.) with scholarships, volunteering
- **4 internships** (Birbal Sahni, Oil India, ONGC, Kumaun University)
- **11 certifications** as cards with Google Drive link placeholders
- **7 field excursions** as chips

Every certificate / reference / volunteering item has `href="#"` placeholders ready for your Google Drive URLs.

---

## 📂 Final file structure

```
your-repo/
├── index.html              ← Full CV homepage
├── assets/
│   └── style.css
├── thesis/
│   └── index.html          ← Research page (no PDF downloads)
├── maps-page/
│   ├── index.html          ← Maps hub
│   ├── live-explorer.html  ← ⭐ ENSEMBLE-based interactive map
│   └── map_*.html          ← 6 placeholder slots for folium maps
├── files/
│   └── Single_BHE_Analysis_GEE_CMIP6_Folium.ipynb
└── data/                   ← Your 16 TIFFs (already on GitHub — DON'T DELETE)
```

---

## 🚀 Deployment

### Step 1: Clean GitHub
On https://github.com/VaibhavJ97/VaibhavJ97.github.io, delete:
- Old `index.html`, `files/`, `maps-page/`, `thesis/`, `assets/`

⚠️ **DO NOT delete** the `data/` folder — your 16 TIFFs are critical for the live map!

### Step 2: Upload v4
1. Unzip `portfolio-site-v4.zip`
2. On GitHub: "Add file" → "Upload files"
3. Open the `portfolio-v4` folder, select all (Ctrl+A), drag in
4. Commit changes
5. Wait 1-2 minutes

### Step 3: Test
Visit https://VaibhavJ97.github.io/maps-page/live-explorer.html

You should see:
1. A loader showing "Fetching BBC (1/8)... CanESM (2/8)..." as it loads all 8 models
2. Once loaded, Germany boundary outlined over a colored map
3. Sidebar shows Mean / P25 / P50 / P75 values
4. Per-model means table at bottom of sidebar
5. **Click on the 4 stat tabs** (Mean / P25 / Median / P75) — map redraws instantly (no re-fetching, it's all cached)
6. **Click anywhere on Germany** — popup shows ALL 4 stats at that point
7. Switch scenario → loads the other 8 models (one-time, then cached)

⏱️ **First load:** ~10-30 seconds depending on your internet (loading 8 TIFFs).
⏱️ **Subsequent stat tab switches:** Instant (cached).
⏱️ **Subsequent scenario switches:** First time = 10-30s, then cached.

---

## 📌 Adding your Google Drive certificate links

Each certificate / reference link in `index.html` has `href="#"`. To replace with real Google Drive URLs:

1. In Google Drive, right-click the file → **Share** → **"Anyone with the link"** → **Copy link**
2. On GitHub, click `index.html` → pencil ✏️ to edit
3. Use Ctrl+F to find the certificate name (e.g., "Python for Data Science")
4. Replace `href="#"` with `href="YOUR_GOOGLE_DRIVE_URL"`
5. Commit changes

**Tip:** You can do this all in one editing session by searching for `href="#"` and replacing each one.

---

## 🎯 What's still using placeholders

In `index.html`, these are `href="#"` placeholders waiting for your URLs:

**Work experience references** (3):
- IONOS reference
- Hydrosion reference  
- KIT student assistant reference

**Education certificates & references** (multiple):
- KIT M.Sc. — certificate, volunteering, scholarship (StipG)
- NIT M.Tech — certificate, project reference, volunteering, scholarship (ONGC)
- B.Sc. — certificate, thesis reference, volunteering, field excursion certificates

**Internship certificates** (4):
- Birbal Sahni Institute — certificate + project reference
- Oil India — certificate
- ONGC — certificate
- Kumaun University — certificate + project reference

**11 certifications**:
- IBM (Sustainability, Python, SQL, PM)
- Datacamp (Power BI x2)
- Microsoft & LinkedIn (Sustainable Tech)
- Atlassian & LinkedIn (Agile)
- Seequent (Leapfrog)
- NPTEL (Remote Sensing)
- KIT (MATLAB)

Send me your Google Drive URLs and I can do a bulk find-and-replace, OR just update them yourself one at a time on GitHub — both ways work.
