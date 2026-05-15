# Vaibhav Jaiswal - Portfolio Homepage

> Personal portfolio website. M.Sc. Applied Geosciences from KIT, with hands-on work in geothermal energy, climate-data modeling, GIS, and web development.

**Live site:** [vaibhavj97.vercel.app](https://vaibhavj97.vercel.app)

---

## About this repo

This is the source for my main portfolio homepage. The site presents my CV, education, work experience, skills, certifications, and links to three project deep-dives:

- [Master Thesis Project](https://vaibhavj97-thesis.vercel.app) - live interactive maps of climate-projected geothermal potential in Germany.
- [GeoChat](https://vaibhavj97-geochat.vercel.app) - AI assistant grounded in the thesis.
- [BHE Recommender](https://vaibhavj97-bhe.vercel.app) - site-specific geothermal feasibility tool.

The four sites form one connected portfolio. This repo hosts only the homepage.

## Features

- Sticky top navigation that links all four sites in the portfolio
- Hero introduction
- About section
- Skills (programming, geospatial, web/tools) with proficiency levels
- Detailed skill blocks (technical, web development, soft skills, languages)
- Experience timeline (IONOS, Hydrosion, KIT)
- Education timeline (KIT, NIT Raipur, BBAU)
- Internships and research projects
- Featured Work CTAs linking to the three companion projects
- Certifications grid
- Field excursions
- Dark 3-column footer (Let's connect / Navigate / Contact)

## Tech stack

- **HTML5 / CSS3** - custom design, no framework
- **Vanilla JavaScript** - minimal, only for small interactions
- **Fonts:** Fraunces (serif), Inter (sans), JetBrains Mono
- **Hosting:** Vercel (free tier), auto-deployed from GitHub

No build step, no Node dependencies, no bundler. The entire site is static.

## How to reproduce locally

Clone the repo and either open `index.html` directly in a browser, or serve it locally:

```bash
git clone https://github.com/VaibhavJ97/VaibhavJ97.github.io.git
cd VaibhavJ97.github.io
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000).

## Project structure

```
VaibhavJ97.github.io/
├── index.html          The main portfolio page
├── assets/
│   ├── style.css       Shared design tokens (colors, typography, layout)
│   └── profile.png     Profile photo
└── README.md           This file
```

## Deploy

Push to `main` and Vercel auto-deploys. No build configuration needed (it's static HTML).

## AI coding assistance disclosure

The site's design, CSS architecture, and HTML structure were developed with [Claude](https://claude.ai) (Anthropic) as a coding partner. The iterative process covered layout decisions, typography choices, accessibility, and code refinement. All design decisions and content are author-written; AI accelerated implementation.

## Author

**Vaibhav Jaiswal**
M.Sc. Applied Geosciences, Karlsruhe Institute of Technology (KIT), 2026

- Email: vaibhavjaiswal1234@gmail.com
- LinkedIn: [linkedin.com/in/vaibhavgeo](https://www.linkedin.com/in/vaibhavgeo/)
- GitHub: [@VaibhavJ97](https://github.com/VaibhavJ97)

## License

Content (CV text, photo) is personal and not for reuse. Code and design are released for academic / personal reference; please credit if you adapt the layout.
