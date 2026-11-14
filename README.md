# Halo Hauling — gohalohauling.com

Website for Halo Hauling: roll-off dumpster rentals & construction debris solutions, Bay Area, CA.

- **Plan:** [docs/plan.md](docs/plan.md)
- **What still needs confirming:** [docs/content-todo.md](docs/content-todo.md)

## Edit from any device
- **Quick text edits:** open the file on github.com → pencil icon → commit. The site redeploys automatically.
- **Business info (phone, emails, cities, prices):** `src/site.ts`
- **Photos:** upload to `public/images/` (names listed in content-todo.md)
- **Pages:** `src/pages/*.astro`

## Status
Planning only. The site has not been built yet; review docs/plan.md first.

## Run locally (once built)
```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # output in dist/
```

## Hosting
Cloudflare Pages (free): connect this repo, build command `npm run build`, output folder `dist`, then add the custom domain gohalohauling.com.

## Quote form
Posts to Web3Forms and emails dispatch@. Set `formKey` in `src/site.ts`.
