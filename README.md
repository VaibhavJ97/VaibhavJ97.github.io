# 🌍 Geothermal Thesis Website — Free Hosting Guide

A complete static website for showcasing your master's thesis on climate change & shallow geothermal energy in Germany. Includes deployment instructions for **100% free** hosting of all your content — including TIFF files, Python notebooks, and GEE scripts.

---

## 📁 What's in this folder

```
geothermal-website/
├── index.html              ← The website (main page)
├── files/                  ← Place your downloadable files here
│   ├── Master_thesis_Vaibhav_Jaiswal.pdf
│   ├── Single_BHE_Analysis_GEE_CMIP6_Folium.ipynb
│   └── GEE_Analysis.pdf
├── maps/                   ← Folium HTML maps go here
│   └── germany_geothermal.html
└── README.md               ← This file
```

---

## 🚀 Recommended Free Hosting Stack

| File type | Hosted on | Limit | Why |
|---|---|---|---|
| Website (HTML/CSS) | **GitHub Pages** | 1 GB site, 100 GB/mo bandwidth | Free, fast CDN, custom domain |
| Thesis PDF | GitHub repo | 100 MB/file | Direct download |
| Python notebooks | GitHub repo | renders natively | Beautiful preview |
| Folium HTML maps | GitHub Pages | unlimited (small) | Interactive, embedded |
| **Large GeoTIFF files** | **Zenodo** | **50 GB / record** | Free, citable DOI, permanent |
| GEE JavaScript | GitHub repo | tiny files | Source control |

---

## ⚡ Quick Start (3 steps, ~15 min)

### Step 1 — Create a GitHub account
Go to **https://github.com/signup** if you don't have one. Free forever.

### Step 2 — Create your site repo
1. Click **+ → New repository**
2. Name it `your-username.github.io` (replace `your-username` with your actual GitHub username — this exact naming is what makes it a free website)
3. Set it to **Public**
4. Click **Create repository**

### Step 3 — Upload everything
1. On your new repo page, click **uploading an existing file**
2. Drag the entire contents of this `geothermal-website/` folder into the upload area
3. Scroll down, click **Commit changes**
4. Wait ~1 minute, then visit: **`https://your-username.github.io`**

🎉 Your website is live!

---

## 📦 Hosting the Large TIFF Files (>100 MB)

GitHub limits individual files to 100 MB. Your CMIP6 GeoTIFFs are likely larger. Use **Zenodo** instead — it's run by CERN, free forever, and gives you a citable DOI (perfect for a thesis!).

### Upload TIFFs to Zenodo:

1. Go to **https://zenodo.org/** and sign in (use GitHub login — easiest)
2. Click **+ New upload**
3. Drag all your `.tif` files (you can upload up to 50 GB per record)
4. Fill in:
   - **Title**: e.g. *"CMIP6 Ground Surface Temperature Projections for Germany (SSP 2-4.5 & 5-8.5)"*
   - **Authors**: Your name
   - **Description**: Brief description from your thesis abstract
   - **License**: Creative Commons Attribution 4.0 (CC-BY-4.0) — most open
   - **Resource type**: Dataset
5. Click **Publish**
6. You'll get a permanent URL like `https://zenodo.org/records/1234567` and a DOI like `10.5281/zenodo.1234567`

### Then update `index.html`:
Find the line with `href="https://zenodo.org/"` and replace it with your actual Zenodo URL.

**Bonus**: A Zenodo DOI lets people *cite* your dataset in their papers — a huge plus for academic visibility.

---

## 🗺️ Generating Folium Maps for the Site

Your notebook already creates folium maps. To embed them on the site:

```python
# In your Jupyter notebook
m = folium.Map(...)
# ... add your layers ...

# Save to the maps/ folder
m.save('maps/germany_geothermal.html')
```

Then commit & push that HTML file to your GitHub repo. It'll be live at:
`https://your-username.github.io/maps/germany_geothermal.html`

---

## 🎨 Customizing the Website

### Change name / contact info
Open `index.html`, search for:
- `Vaibhav Jaiswal` → your name
- `your.email@example.com` → your email
- `https://github.com/` → your GitHub profile
- LinkedIn / ORCID — replace `#` with your actual links

### Change colors
At the top of `index.html` (in `<style>`), modify the CSS variables:
```css
--accent: #b8501e;       /* terracotta — change to any color */
--earth: #3d5a3d;        /* deep forest green */
```

### Change the hero text
Search for `Climate change & the future of` in `index.html` and edit.

---

## 🔗 Custom Domain (Optional, $0–12/year)

Want `vaibhavjaiswal.com` instead of `username.github.io`?

1. Buy a domain at **Namecheap**, **Porkbun**, or **Cloudflare** (~$10/year)
2. In your GitHub repo: **Settings → Pages → Custom domain** → enter your domain
3. Add the DNS records GitHub shows you to your domain registrar
4. Done — HTTPS is free & automatic via GitHub

---

## 📋 File Hosting Summary — What Goes Where

| Your file | Where to put it | URL pattern |
|---|---|---|
| `Master_thesis.pdf` | `files/` in GitHub repo | `username.github.io/files/Master_thesis.pdf` |
| `analysis.ipynb` | `files/` in GitHub repo | renders on github.com automatically |
| `GEE_script.js` | `files/` in GitHub repo | direct view + download |
| `output_map.html` (folium) | `maps/` in GitHub repo | `username.github.io/maps/output_map.html` |
| `BBC_ssp245.tif` (large) | **Zenodo** | `zenodo.org/records/XXXXX` |
| `CanESM_ssp585.tif` (large) | **Zenodo** (same record) | same URL, list all together |

---

## 🆘 Alternative Free Hosts (if you don't want GitHub)

| Platform | Best for | Note |
|---|---|---|
| **Netlify** | Drag-and-drop deploy | 100 GB bandwidth/mo, free |
| **Cloudflare Pages** | Same as GitHub Pages | Unlimited bandwidth |
| **Vercel** | Same idea, very fast | Free for personal use |
| **Hugging Face Spaces** | If you want to add a Python demo too | Free GPU/CPU options |

For TIFFs specifically, alternatives to Zenodo:
- **Figshare** — similar to Zenodo, also free with DOI
- **Open Science Framework (OSF)** — free, 50 GB
- **Hugging Face Datasets** — free, unlimited (great for ML)

---

## ✅ Final Checklist Before Going Live

- [ ] Replaced "your.email@example.com" with real email
- [ ] Updated GitHub link in footer
- [ ] Uploaded TIFFs to Zenodo, got DOI, updated link in `index.html`
- [ ] Generated & added folium maps to `maps/` folder
- [ ] Tested site on mobile (it's responsive — should work)
- [ ] Added thesis PDF to `files/` folder
- [ ] (Optional) Custom domain configured

---

**Built with ❤️ for open science.**
