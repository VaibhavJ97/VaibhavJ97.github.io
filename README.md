# Portfolio Homepage - Vaibhav Jaiswal

> Personal portfolio for Vaibhav Jaiswal. Vanilla HTML, CSS, JavaScript. Hosted on Vercel.

**Live**: [vaibhavj97.vercel.app](https://vaibhavj97.vercel.app)

## What this is

The front door of my online portfolio. Cross-links to 3 other deployed projects (Master's Thesis page, GeoChat, BHE Recommender). Designed to position me as a developer with a geoscience background, not the other way around.

## Tech stack

| Layer | What |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (custom, no framework) |
| Scripting | Vanilla JavaScript (no build step) |
| Code highlighting | Prism.js (Tomorrow theme, via CDN) |
| Fonts | Fraunces, Inter, JetBrains Mono (all from Google Fonts) |
| Analytics | Vercel Web Analytics |
| Hosting | Vercel (auto-deploys from `main` branch) |

## Sections (top to bottom)

- Hero with positioning statement
- About
- § 02 Featured Work (3 clickable project cards)
- Project metrics strip
- Open to Roles callout with availability, work permit, notice period, Calendly booking
- § 03 Skills and Tools
- Currently exploring
- § 04 Code samples (real Python and Node.js snippets, syntax-highlighted)
- § 05 Experience (IONOS, Hydrosion, KIT IAG)
- § 06 Education (M.Sc. KIT, B.Sc. AKTU)
- § 07 Certifications
- § 08 Writing (planned blog posts)
- Footer with email, LinkedIn, GitHub, Calendly

## Why no framework

The site is content-heavy and static. React, Vue, or Next.js would add a build step, bundling, hydration, and runtime overhead for no real benefit. Vanilla HTML/CSS/JS loads in under a second, deploys instantly on every push, and stays simple to maintain. The Featured Work cards demonstrate that I can build a clickable, accessible, hover-animated component with 20 lines of HTML and CSS instead of 200 lines of React.

## Accessibility features

- Skip-to-content link (visible on keyboard focus)
- Focus rings on all interactive elements including the clickable project cards
- Semantic HTML (header, main, footer, nav, section)
- JSON-LD Person schema for SEO and assistive technologies
- Open Graph and Twitter Card meta tags with a 1200x630 preview image
- Responsive: tested on phone, tablet, desktop

## Run locally

```bash
git clone https://github.com/VaibhavJ97/VaibhavJ97.github.io.git
cd VaibhavJ97.github.io
python3 -m http.server 8000
# Open http://localhost:8000
```

No `npm install`, no environment variables, no secrets.

## Project structure

```
.
├── index.html         # The homepage (single file)
├── og-preview.png     # 1200x630 social-media preview image
├── assets/
│   └── style.css      # External stylesheet (some styles inlined in index.html)
└── README.md
```

## License

MIT. Use any design or code you find useful.

## About me

I'm Vaibhav, a Web Developer with a Master's in Applied Geosciences from KIT. Working Student at IONOS SE in Karlsruhe. Open to roles in Python, web development, data engineering, and AI integration.

[Portfolio](https://vaibhavj97.vercel.app) · [LinkedIn](https://www.linkedin.com/in/vaibhavgeo/) · [Book a call](https://calendly.com/vaibhavjaiswal1234/30min) · [Email](mailto:vaibhavjaiswal1234@gmail.com)
