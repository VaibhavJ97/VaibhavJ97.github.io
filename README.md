# 🚀 Portfolio Site v3 — What's New

## ✨ Major upgrades

### 1. 🎯 LIVE Interactive Map Explorer (NEW!)
A fully interactive map at `/maps-page/live-explorer.html` that:
- Reads your TIFF files directly from the GitHub `data/` folder
- Has **dropdowns** to switch between climate models (BBC, CanESM, GFDL, GISS, HadGEM, IPSL, MIROC, MPI)
- Has **dropdowns** to switch between SSP 2-4.5 / SSP 5-8.5 scenarios
- Has **dropdowns** for 5 different colormaps (Viridis, Magma, Plasma, Reds, Thermal)
- **Click anywhere on the map** to query the temperature at that point
- Shows live stats (min/max/mean temperature)
- Zero server needed — pure browser-based!

This is exactly like having your Jupyter notebook dropdowns on a public webpage.

### 2. 📋 Real CV Content
Homepage now uses your actual experience from both CVs:
- IONOS SE (Web Dev / TYPO3)
- Hydrosion GmbH (Geothermal exploration)
- KIT Institute of Applied Geosciences (Lab work)
- KIT M.Sc. (with full thesis details)
- B.Sc. from Babasaheb Bhimrao Ambedkar University

### 3. 📥 BOTH CVs available for download
Two prominent download cards on the homepage:
- `Vaibhav_CV.pdf` — Geoscience focus
- `Vaibhav_CV_Dev.pdf` — Web development focus

### 4. ✅ Real contact info baked in
- Email: vaibhavjaiswal1234@gmail.com
- Phone: +49 151 4338 3819
- Address: Rheinstraße 30, 76185 Karlsruhe
- GitHub: VaibhavJ97

---

## 📂 Final folder structure

```
your-repo/
├── index.html              ← HOME (CV intro, skills, experience, education, certs)
├── assets/
│   └── style.css           ← Shared styles
├── thesis/
│   └── index.html          ← RESEARCH page
├── maps-page/
│   ├── index.html          ← MAPS HUB (with featured live explorer)
│   ├── live-explorer.html  ← ⭐ NEW! Live interactive map with dropdowns
│   └── map_*.html          ← 6 placeholder slots for folium maps
├── files/
│   ├── Master_thesis_Vaibhav_Jaiswal.pdf
│   ├── Single_BHE_Analysis_GEE_CMIP6_Folium.ipynb
│   ├── GEE_Analysis.pdf
│   ├── Vaibhav_CV.pdf       ← NEW
│   └── Vaibhav_CV_Dev.pdf   ← NEW
└── data/                    ← Your 16 TIFFs (already on GitHub)
```

---

## 🚀 How to deploy

### Step 1: Wipe your existing site files
Go to https://github.com/VaibhavJ97/VaibhavJ97.github.io and delete:
- The old `index.html`
- The old `files/` folder (we'll re-upload with CVs added)
- The old `maps/` folder (replaced by `maps-page/`)
- The old `thesis/` folder if it exists
- The old `assets/` folder if it exists

⚠️ **DO NOT DELETE** the `data/` folder! Your 16 TIFFs are there and the live explorer needs them.

### Step 2: Upload new files
1. Click "Add file" → "Upload files"
2. Open the unzipped `portfolio-v3` folder
3. Select ALL contents (Ctrl+A) — including all subfolders
4. Drag into GitHub upload area
5. Commit changes

### Step 3: Test the live explorer
1. Wait 1-2 minutes for GitHub Pages to rebuild
2. Visit: `https://VaibhavJ97.github.io/maps-page/live-explorer.html`
3. You should see a map of Germany with temperature colors
4. Try changing the dropdowns!

If the map shows an error like "file not found":
- Make sure your `data/` folder still has the TIFFs
- Make sure the repo is **Public** (Settings → General)

---

## 🎨 Customization tips

### Add your photo
1. Save your photo as `profile.jpg` (square or 4:5 ratio works best)
2. Upload it to the `assets/` folder on GitHub
3. Edit `index.html`: find the `<div class="placeholder">` section and replace with:
   ```html
   <img src="assets/profile.jpg" alt="Vaibhav Jaiswal">
   ```

### Add LinkedIn URL
In `index.html`, search for "LinkedIn" — currently no LinkedIn link is in the file because I didn't see one in your CV. You can add one in the contact strip and footer easily.

### Replace placeholder folium maps
The 6 map cards still link to placeholder files. To replace them with real folium maps from your notebook:
```python
m.save('map_ssp245_50yr_extraction.html')
# etc for each scenario
```
Upload these files to `maps-page/` folder, replacing the placeholders.

---

## 🔧 How the LIVE explorer works (technical)

The live map uses three open-source JS libraries (no server needed):
- **Leaflet.js** — the map renderer
- **georaster + georaster-layer-for-leaflet** — reads GeoTIFFs directly in the browser
- **chroma-js** — color scale generation

When you change a dropdown, the JavaScript:
1. Constructs the filename: `{Model}_{scenario}_2000_2100_Germany_mean.tif`
2. Fetches it from `https://VaibhavJ97.github.io/data/{filename}`
3. Parses the GeoTIFF with georaster
4. Computes min/max/mean stats
5. Renders the raster with the chosen colormap
6. Adds click-to-query interactivity

Total file size: ~5-15 MB per TIFF, loads in 1-3 seconds on average broadband.
