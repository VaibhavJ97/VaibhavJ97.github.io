# Portfolio Homepage - Vaibhav Jaiswal

> Personal portfolio for Vaibhav Jaiswal. Vanilla HTML, CSS, JavaScript. Hosted on Vercel.

**Live**: [vaibhavj97.vercel.app](https://vaibhavj97.vercel.app)

## What this is

The front door of my online portfolio. Cross-links to 3 other deployed projects (GeoChat, BHE Recommender, and the thesis data-pipeline app). Positions me as a software developer working across Python, JavaScript, and AI integration.

## Tech stack

| Layer | What |
|---|---|
| Markup | HTML5 (semantic, accessible) |
| Styling | CSS3 (custom design system, no framework) |
| Scripting | Vanilla JavaScript (no build step) |
| Code highlighting | Hand-authored `<span>` token markup (no JS highlighter) |
| Fonts | Newsreader, IBM Plex Sans, IBM Plex Mono (Google Fonts) |
| Analytics | Vercel Web Analytics |
| Hosting | Vercel (auto-deploys from `main` branch) |
| Development | AI-pair-programming (Claude, ChatGPT, GitHub Copilot) with full manual review |

## How this site was built

I built this with **AI-assisted development workflows** - Anthropic Claude as the primary pair-programmer, ChatGPT for ideation and copy iteration, and GitHub Copilot for inline suggestions. The architecture decisions (vanilla stack, accessibility-first, no framework), the design system (cream + ink + green palette, Newsreader + IBM Plex), and the content (every word) are mine. The code generation, refactoring, and iteration loops were AI-accelerated.

This workflow is part of the stack I bring to my next role.

## Architecture

Single-file static site. No backend, no database, no build step. The browser fetches `index.html`, which inlines all CSS and pulls fonts from Google Fonts. Vercel auto-deploys on every push to `main`. Served from the CDN edge with a sub-second first paint.

The 4 sites in the portfolio (this homepage + 3 project sites) are independent Vercel projects but visually consistent. They cross-link via the navigation bar and footer.

## Sections (top to bottom)

- Hero positioning statement (Software Developer · Python · JavaScript · AI Integration)
- About
- § 02 Featured Work (4 clickable project cards)
- Project metrics strip
- Open to Roles callout with availability, work permit, notice period, Calendly booking
- § 03 Skills & Tools (Languages & Backend, Web & Frontend, AI & LLM Integration, Data & Tooling)
- Currently exploring
- § 04 Code samples (real Node.js and Python snippets, syntax-highlighted)
- § 05 Experience (IONOS, Hydrosion, KIT)
- § 06 Education (M.Sc. KIT, B.Sc. BBAU)
- § 07 Certifications
- Footer with email, LinkedIn, GitHub, Calendly

## Why no framework

The site is content-heavy and static. React, Vue, or Next.js would add a build step, bundling, hydration, and runtime overhead for no real benefit. Vanilla HTML/CSS/JS loads in under a second, deploys instantly on every push, and stays simple to maintain. The Featured Work cards demonstrate that I can build a clickable, accessible, hover-animated component with a handful of lines of HTML and CSS instead of a pile of React.

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
├── index.html         # The homepage (single file, CSS inlined)
├── og-home.png        # 1200x630 social-media preview image
├── profile-photo.png  # About section photo
└── README.md
```

## License

MIT. Use any design or code you find useful.

## Disclaimer

This is a personal portfolio, not a production application. Code is provided as-is. The claims describe my own work and ownership; the AI-assisted parts of the workflow are disclosed transparently.

## About me / Contact

I'm Vaibhav, a software developer building AI-integrated apps, serverless backends, and interactive web tools in Python, JavaScript, and Node.js. Working Student at IONOS SE in Karlsruhe. Open to roles in software engineering, full-stack / web development, Python / backend, and AI / LLM integration.

- **Email**: vaibhavjaiswal1234@gmail.com
- **Portfolio**: [vaibhavj97.vercel.app](https://vaibhavj97.vercel.app)
- **LinkedIn**: [linkedin.com/in/vaibhavgeo](https://www.linkedin.com/in/vaibhavgeo/)
- **GitHub**: [github.com/VaibhavJ97](https://github.com/VaibhavJ97)
- **Book a 30-min call**: [calendly.com/vaibhavjaiswal1234/30min](https://calendly.com/vaibhavjaiswal1234/30min)
- **Location**: Karlsruhe, Germany

### My other repos

- [GeoChat](https://github.com/VaibhavJ97/geochat) - RAG-style AI chatbot with a Node.js serverless backend and Gemini
- [BHE Recommender](https://github.com/VaibhavJ97/bhe-recommender) - interactive map tool with in-browser cost model, LLM interpretation, and PDF export
- [Thesis Data Pipeline](https://github.com/VaibhavJ97/kit-master-thesis-portfolio) - Python (NumPy/SciPy) pipeline exporting JSON for a live Leaflet.js frontend
