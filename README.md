# aimanasyraf-portfolio

The source for my personal portfolio website: who I am, what I've built, and how to reach me.

> **Status:** first version: a single page with About, Projects, Experience and Contact.

## About

I'm Aiman Asyraf, a third-year student at Universiti Teknologi PETRONAS (UTP),
currently interning at ams OSRAM in SAP Authorization.

## Projects

| Project | What it is | Stack |
|---|---|---|
| **Neekah** | A two-sided wedding marketplace for the Muslim/nikah market in Southeast Asia, where couples find vendors and send booking requests | Flutter, Rails API, Supabase |

## Tech stack

- [Astro](https://astro.build): static site framework
- [Cloudflare Pages](https://pages.cloudflare.com): hosting

## Running locally

Requires Node.js 22.12 or newer (see `.nvmrc`) and npm.

```bash
git clone https://github.com/AimxnAsyraf/aimanasyraf-portfolio.git
cd aimanasyraf-portfolio
npm install
npm run dev       # start the dev server with live reload
```

| Command | What it does |
|---|---|
| `npm run dev` | Start the local dev server |
| `npm run build` | Build the static site into `dist/` |
| `npm run preview` | Serve the built `dist/` locally (run `build` first) |
| `npm run deploy` | Build and deploy to Cloudflare Pages with Wrangler |

## Project structure

```
src/
  data.ts              # all site content: profile, experience, projects
  pages/index.astro    # the home page
  layouts/Base.astro   # <html>/<head> wrapper
  components/          # reusable pieces (Section)
  styles/global.css    # colours, light/dark theme, layout
public/                # static files copied as-is (favicon)
wrangler.jsonc         # Cloudflare Pages config
```

To update the content, edit `src/data.ts`. To add a project, add an entry to `projects`.

## Deployment

Hosted on **Cloudflare Pages**, connected to this repo. Pushes to `main` deploy automatically;
other branches get preview deployments. Config lives in `wrangler.jsonc`.

| Setting (Pages project → Settings → Build) | Value |
|---|---|
| Framework preset | Astro |
| Build command | `npm run build` |
| Build output directory | `dist` |

Manual deploy from your machine: `npm run deploy` (needs `npx wrangler login` first).

**Live URL:** https://aimanasyraf-portfolio.pages.dev (custom domain coming later).

## Contact

- Email: [aimanasyraf115@gmail.com](mailto:aimanasyraf115@gmail.com)
- LinkedIn: [Aiman Asyraf Zulkefli](https://www.linkedin.com/in/aiman-asyraf-zulkefli-a698772b4/)
- GitHub: [@AimxnAsyraf](https://github.com/AimxnAsyraf)

## License

© Aiman Asyraf. All rights reserved.
