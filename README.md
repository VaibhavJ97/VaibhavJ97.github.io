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
| Development | AI-pair-programming (Claude, ChatGPT, GitHub Copilot) with full manual review |

## How this site was built

I built this with **AI-assisted development workflows** - using Anthropic Claude as the primary pair-programmer, ChatGPT for ideation and copy iteration, and GitHub Copilot for inline suggestions. The architecture decisions (vanilla stack, accessibility-first, no framework), the design system (cream + ink + orange palette, Fraunces + Inter + JetBrains Mono), and the content (every word) are mine. The code generation, refactoring, and iteration loops were AI-accelerated.

This workflow is part of the stack I bring to my next role.

## Architecture

Single-file static site. No backend, no database, no build step. The browser fetches `index.html`, which inlines critical CSS and pulls fonts from Google Fonts and syntax highlighting from cdnjs. Vercel auto-deploys on every push to `main`. Total runtime: served from CDN edge, < 1 second first paint.

The 4 sites in the portfolio (this homepage + 3 project sites) are independent Vercel projects but visually consistent. They cross-link via the navigation bar and footer.

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
├── profile-photo.png  # About section photo
├── assets/
│   └── style.css      # External stylesheet (some styles inlined in index.html)
└── README.md
```

## License

MIT. Use any design or code you find useful.

## Disclaimer

This is a personal portfolio, not a production application. Code is provided as-is. The "What I bring" claims describe my own work and ownership; the AI-assisted parts of the workflow are disclosed transparently.

## About me / Contact

I'm Vaibhav, a Web Developer with a Master's in Applied Geosciences from KIT. Working Student at IONOS SE in Karlsruhe. Open to roles in Python, web development, data engineering, and AI integration.

- **Email**: vaibhavjaiswal1234@gmail.com
- **Portfolio**: [vaibhavj97.vercel.app](https://vaibhavj97.vercel.app)
- **LinkedIn**: [linkedin.com/in/vaibhavgeo](https://www.linkedin.com/in/vaibhavgeo/)
- **GitHub**: [github.com/VaibhavJ97](https://github.com/VaibhavJ97)
- **Book a 30-min call**: [calendly.com/vaibhavjaiswal1234/30min](https://calendly.com/vaibhavjaiswal1234/30min)
- **Location**: Karlsruhe, Germany

### My other repos

- [Master Thesis Project](https://github.com/VaibhavJ97/kit-master-thesis-portfolio) - interactive climate-geothermal maps
- [GeoChat](https://github.com/VaibhavJ97/geochat) - AI chatbot grounded in my thesis
- [BHE Recommender](https://github.com/VaibhavJ97/bhe-recommender) - geothermal feasibility tool with PDF report
