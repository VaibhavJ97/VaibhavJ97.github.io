# Portfolio Site v8 - Live JS-Rendered Map Explorer

## What's new in v8

- ✅ **Live color switching** with 9 heat colormaps + 7 power colormaps
- ✅ **Real layer toggles** (checkboxes that actually show/hide map layers)
- ✅ **Click any pixel** to see exact W/m or W value
- ✅ **Real BHE simulation output** (not fake JS rendering of TIFFs)
- ✅ Same Master Thesis Project page structure as v7
- ✅ Germany boundary
- ✅ All 8 models + 2 scenarios + 4 ensemble stats

## How it works

```
Python notebook (run once locally)
    |
    v
export_to_json.py exports model arrays as compact JSON
    |
    v
Upload data_json/ folder to GitHub
    |
    v
JavaScript fetches JSON + renders with Leaflet + chroma-js
    |
    v
User changes colormap -> instant re-render (no Python needed)
```

## ONE-TIME SETUP (~5 minutes total)

### Step 1: Get the model variables loaded in your notebook
Open `Single_BHE_Analysis_GEE_CMIP6_Folium.ipynb` and run all cells from top to bottom. Make sure you have all the variables: `BBC_ssp245`, `BBC_ssp585`, `CanESM_ssp245`, ... up to `MPI_ssp585`.

If MPI cells (33-36) and ensemble cells (37-38) haven't run yet, run them now.

### Step 2: Run the export script
In the SAME notebook (so the variables are still in memory), add a new cell at the bottom and paste:

```python
exec(open('export_to_json.py').read())
```

(The `export_to_json.py` file is in the `files/` folder of this zip - copy it next to your notebook first.)

This takes about 30 seconds and creates a `data_json/` folder with:
- `meta.json` (1 KB)
- `individual/*.json` (16 files, ~70 KB each)
- `ensemble/*.json` (8 files, ~70 KB each)

Total: about 1.7 MB

### Step 3: Upload to GitHub
1. The script created a `data_json/` folder next to your notebook
2. Upload the ENTIRE `data_json/` folder to your GitHub repo at: `thesis/data_json/`
   - So the final paths are like: `thesis/data_json/individual/BBC_ssp245.json`
3. Commit and wait 1-2 minutes for GitHub Pages to redeploy

### Step 4: Visit your site
The live explorer at `https://VaibhavJ97.github.io/thesis/#explorer` now works!
- Switch climate models, scenarios -> instant
- Switch colormaps -> instant
- Toggle layers -> instant
- Click any point on the map -> popup with exact values

## Deployment

1. Go to https://github.com/VaibhavJ97/VaibhavJ97.github.io
2. Delete: old `index.html`, `files/`, `thesis/`, `assets/` (KEEP the `data/` folder!)
3. Unzip this `portfolio-site-v8.zip`
4. Upload all contents of the `portfolio-v8` folder
5. Commit
6. Run the export script locally (one time)
7. Upload `data_json/` folder

## File structure

```
your-repo/
├── index.html              (Full CV homepage)
├── assets/
│   └── style.css
├── thesis/
│   ├── index.html          (Master Thesis Project + JS-rendered explorer)
│   └── data_json/          (Created after running export script)
│       ├── meta.json
│       ├── individual/
│       │   ├── BBC_ssp245.json
│       │   └── ... 16 files
│       └── ensemble/
│           ├── ssp245_mean.json
│           └── ... 8 files
├── files/
│   ├── Single_BHE_Analysis_GEE_CMIP6_Folium.ipynb
│   └── export_to_json.py   (One-time script)
└── data/                   (Your 16 TIFFs, untouched)
```
