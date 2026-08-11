# Geoscience Portfolio Homepage - Vaibhav Jaiswal

> Geoscience portfolio for Vaibhav Jaiswal. Vanilla HTML, CSS, JavaScript. Hosted on Vercel, with routed sub-apps served from their own repositories.

**Live**: [vaibhavjgeo.vercel.app](https://vaibhavjgeo.vercel.app)

## What this is

The front door of my geoscience portfolio. Positions me as a geoscientist working across geospatial data science, climate and subsurface modelling, and research software. Three project pages (Master Thesis, BHE Recommender, GeoChat) live in their own repositories and are served under this domain via Vercel rewrites - one visible website, four independent codebases.

## Tech stack

| Layer | What |
|---|---|
| Markup | HTML5 (semantic, accessible) |
| Styling | CSS3 (custom design system, no framework) |
| Scripting | Vanilla JavaScript (no build step) |
| Routing | Vercel rewrites (`/thesis`, `/bhe`, `/geochat` proxied to sibling projects) |
| Fonts | Newsreader, IBM Plex Sans, IBM Plex Mono (Google Fonts) |
| Analytics | Vercel Web Analytics |
| Hosting | Vercel (auto-deploys from `main`) |
| Development | AI-pair-programming (Claude, Copilot) with full manual review |

## How this site was built

Built with **AI-assisted development workflows** - Anthropic Claude as the primary pair-programmer for code generation, refactoring, and the multi-repo rewrite architecture. The design system (cream + ink + green palette, Newsreader + IBM Plex), the scientific content (every number comes from my thesis), and the architecture decisions are mine. AI accelerated the iteration loops.

## Architecture

Single-file static homepage plus a `vercel.json` that proxies three routes to independent Vercel projects:

```
vaibhavjgeo.vercel.app
├── /            -> this repo (index.html)
├── /thesis/*    -> vaibhavjgeo-thesis   (repo: master-thesis)
├── /bhe/*       -> vaibhavjgeo-bhe      (repo: bhe-recommender)
├── /geochat/*   -> vaibhavjgeo-geochat  (repo: geochat)
└── /api/*       -> proxied to the owning app's serverless function
```

The visitor never leaves the domain; each app keeps its own repository, deploy pipeline, and history.

## Sections (top to bottom)

- Hero positioning statement (Geoscientist · Geospatial Data Science · Climate & Subsurface Modelling)
- About - from field geology to geospatial data science
- § 02 Research & Applied Work (3 clickable project cards)
- Research metrics strip (8 CMIP6 models, 5 km grid, 100-yr horizons)
- § 03 Skills & Methods (Geoscience & Modelling, Geospatial & Remote Sensing, Programming & Data, AI for Science)
- § 04 Methods in Code (Python extraction solver, Earth Engine CMIP6 export)
- § 05 Experience (IONOS, Hydrosion / EnBW Bruchsal, KIT)
- § 06 Education (M.Sc. KIT, B.Sc. BBAU)
- § 07 Certifications
- Footer with email and GitHub

## Run locally

```bash
git clone https://github.com/vaibhavjgeo/geoscience-portfolio.git
cd geoscience-portfolio
python3 -m http.server 8000
# Open http://localhost:8000
```

No `npm install`, no environment variables, no secrets. (The `/thesis`, `/bhe`, `/geochat` routes only resolve on Vercel, where the rewrites run.)

## Project structure

```
.
├── index.html         # The homepage (single file, CSS inlined)
├── vercel.json        # Rewrites to the three sibling projects
├── profile-photo.png  # About section photo
└── README.md
```

## License

MIT. Use any design or code you find useful.

## Disclaimer

This is a personal portfolio, not a production application. Code is provided as-is. Scientific figures cited on the page come from my M.Sc. thesis and are described there with full methodology and limitations.

## About me / Contact

I'm Vaibhav, a geoscientist (M.Sc. Applied Geosciences, KIT) modelling climate-change impacts on the shallow subsurface with Python, GIS, and Google Earth Engine. Open to PhD positions and research roles in geospatial data science, climate and subsurface research, and geoenergy.

- **Email**: vaibhavjaiswal1234@gmail.com
- **Portfolio**: [vaibhavjgeo.vercel.app](https://vaibhavjgeo.vercel.app)
- **LinkedIn**: [linkedin.com/in/vaibhavgeo](https://www.linkedin.com/in/vaibhavgeo/)
- **GitHub**: [github.com/vaibhavjgeo](https://github.com/vaibhavjgeo)
- **Location**: Karlsruhe, Germany

### The other repos in this portfolio

- [master-thesis](https://github.com/vaibhavjgeo/master-thesis) - CMIP6 x geothermal modelling results as an interactive atlas
- [bhe-recommender](https://github.com/vaibhavjgeo/bhe-recommender) - click-anywhere geothermal feasibility tool with LLM interpretation and PDF export
- [geochat](https://github.com/vaibhavjgeo/geochat) - AI assistant grounded in my thesis research
