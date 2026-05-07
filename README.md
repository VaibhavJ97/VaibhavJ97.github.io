# Portfolio Site v7 - Final Master Thesis Project Edition

## What changed in v7

### Structure
- **"Research" page renamed to "Master Thesis Project"** (in nav and on the page)
- **Map explorer is now part of Master Thesis Project page** (no separate Maps page)
- **No "Contact" link in nav** anymore - contact info is in every footer
- Old `maps-page/` folder deleted, contents merged into `thesis/`

### Map Explorer enhancements
1. **Color scale legends now span full width**, layout in two lines (label on top, gradient below, values below that)
2. **9 Heat Extraction color schemes** to choose from: Viridis, Plasma, Inferno, Magma, Cividis, Turbo, YlGnBu, BuGn, Coolwarm
3. **7 Usable Power color schemes**: Reds, Oranges, YlOrRd, PuRd, Hot, Autumn, Copper
4. **Sidebar layer swatches update live** when color scheme changes
5. The map iframe itself shows the original notebook colors (viridis + Reds), since those are baked in

### Footer (every page)
- Email: vaibhavjaiswal1234@gmail.com
- GitHub Repository link (https://github.com/VaibhavJ97/VaibhavJ97.github.io)
- LinkedIn link (https://www.linkedin.com/in/vaibhavgeo/)
- "Maps - folium - Leaflet.js" line removed
- "Languages" line removed from homepage footer

### Typography
- **Every em dash (-) replaced with hyphen (-)** across all pages
- This rule will be followed in all future content

---

## Files & structure

```
your-repo/
├── index.html                       (Full CV homepage)
├── assets/
│   └── style.css
├── thesis/
│   ├── index.html                   (Master Thesis Project page + map explorer)
│   ├── individual/                  (16 maps - 14 real, 2 placeholders)
│   │   ├── BBC_ssp245.html
│   │   ├── BBC_ssp585.html
│   │   ├── ... (14 real folium maps)
│   │   ├── MPI_ssp245.html          (placeholder - notebook cell never run)
│   │   └── MPI_ssp585.html          (placeholder)
│   └── ensemble/                    (8 placeholders)
│       ├── ssp245_mean.html
│       ├── ssp245_p25.html
│       ├── ssp245_p50.html
│       ├── ssp245_p75.html
│       └── ssp585_*.html (4 more)
├── files/
│   └── Single_BHE_Analysis_GEE_CMIP6_Folium.ipynb
└── data/                            (your 16 TIFFs - already on GitHub, keep!)
```

---

## How to deploy

1. Go to https://github.com/VaibhavJ97/VaibhavJ97.github.io
2. Delete: old `index.html`, `files/`, `maps-page/`, `thesis/`, `assets/` (KEEP the `data/` folder!)
3. Unzip `portfolio-site-v7.zip`
4. Upload all contents from `portfolio-v7/` folder to GitHub (drag whole folder contents)
5. Commit
6. Wait 1-2 minutes
7. Visit:
   - Homepage: https://VaibhavJ97.github.io
   - Master Thesis Project: https://VaibhavJ97.github.io/thesis/

The map explorer is now part of the Master Thesis Project page (scroll down or click "Explore the live maps" button).

---

## How the map explorer works

### Sidebar (left, 380px wide)
- Mode tabs: Individual model | Ensemble
- Model dropdown (8 GCMs) or Statistic dropdown (Mean/P25/P50/P75)
- Scenario dropdown (SSP 2-4.5 / SSP 5-8.5)
- **Heat Extraction color scheme picker** (9 options)
- **Usable Power color scheme picker** (7 options)
- 6 toggleable layers info (with color swatches that update with scheme)
- Source links

### Top of map area (full width)
- Two color scale legends side by side
- Each shows: scheme name on top, gradient bar in middle, value markers below

### Main area (right, fills the rest)
- Iframe loading the chosen folium HTML
- The actual map keeps its notebook colors (viridis for heat, Reds for power)
- All 6 togglable layers visible inside the map
- Germany boundary
- Layer toggle in top-right

---

## Important note about color schemes

The **map iframe itself** uses the colors that were saved when the notebook was run (viridis for heat, Reds for power). Those are baked into the HTML files.

The **website's color scheme picker** updates:
- The two color legends at the top
- The 6 layer info swatches in the sidebar

This way visitors can see how the data would look with different palettes, even if the iframe uses the originals. To get the iframe colors to actually change, you would need to re-run the notebook with different `cmap_name=` values and re-extract.

---

## To complete the missing 10 maps later

Run cells 33-38 in the notebook on your local machine. Then either:
- Send me the updated notebook so I can re-extract, or
- Right-click each rendered map in Jupyter, save the HTML, upload to the matching folder
