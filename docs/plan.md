# Halo Hauling Website — Plan

## Context
New Bay Area roll-off dumpster business (owners: you + your wife). Only presence today is Instagram @halohauling. Goal: a fast, mobile-first site on **gohalohauling.com** that turns visitors into quote requests, built in a GitHub repo so you can work from any device.

Decisions made:
- **Static site in GitHub** (Astro + plain CSS), free hosting on Cloudflare Pages, auto-deploys on push.
- **Domain: gohalohauling.com** (the one you own). Emails: info@ / dispatch@ / billing@gohalohauling.com via Google Workspace (dispatch + billing can alias to one inbox at first).
- **Repo:** you create empty `HaloHauling/website` on github.com (create free org "HaloHauling" first if needed); I attach and push.
- **Instagram:** allow instagram.com in this environment so I can try to review it (Instagram often blocks bots — fallback: you upload the 6 job photos + logo).

## Step 0 — Setup (needs you)
1. Approve adding `www.instagram.com` + `instagram.com` to the environment allowlist; I review profile, captions, hashtags, photos.
2. Create `HaloHauling/website` (empty, private OK). I attach it with push access.
3. Send logo file (green/gold winged-H) and the 6 real job photos.

## Branding
- Colors: bright dumpster blue (primary/CTA), dark green + gold (from logo, header/footer/accents), white/light gray backgrounds.
- Taglines: "Your Project. Our Priority." and "Find Your Perfect Fit."
- Real photos only, no stock.

## Site map (pages)
1. **Home / Request a Quote** (`/`)
2. **Dumpster Sizes & Pricing** (`/dumpster-sizes`)
3. **Construction & Demolition Debris** (`/construction-demolition`)
4. **LEED Recycling Reports** (`/leed-recycling-reports`)
5. **Green Halo Reporting Support** (`/green-halo-reporting`)
6. **Service Areas** (`/service-areas`)
7. **Contact Us** (`/contact`)

### Shared header / footer
- Header: logo + name, nav, Instagram icon, sticky **Get a Quote** button (stays visible on mobile) + tap-to-call once phone is set.
- Footer: Halo Hauling · Bay Area, CA · services list · Instagram · info@/dispatch@/billing@ · disclaimer: "Green Halo is a trademark of Green Halo Systems. Halo Hauling is not affiliated with Green Halo Systems."

### Home page sections
1. Hero: **HALO HAULING** / *Roll-Off Dumpster Rentals & Construction Debris Solutions* / *C&D Recycling • LEED Documentation • Green Halo Reporting Support*; secondary line "Your Project. Our Priority."; buttons Get a Quote / Message Us on Instagram; real truck/dumpster photo.
2. Trust bar: Roll-Off Dumpsters | Construction & Demolition | Dirt & Concrete | Residential & Commercial Cleanouts
3. Services — 4 cards (2 lines each: what / who)
4. Find Your Perfect Fit — size guide 10/15/20/30/40-yd with use cases; "Not sure? Message us" (no guessed prices)
5. How it works — 3 steps
6. Who it's for — Homeowners / Contractors / Businesses
7. Service area — "Bay Area, CA" (San Jose only once confirmed)
8. Real work — 6 photos + link to Instagram
9. FAQ — cost, rental length, allowed/prohibited items, driveway protection, delivery speed (answers marked TBD for you to fill)
10. **Quote form** (see below) + "Prefer to talk? Message us on Instagram @halohauling"

### Quote form fields
Name, Phone, Email, Service needed, Dumpster size (10/15/20/30/40/Not sure), Material (C&D mixed, dirt, concrete, household/cleanout, other), Delivery address/location, Requested date, Details/notes, LEED or Green Halo docs needed? (yes/no).
Delivery: free form backend (Web3Forms or Formspree) → emails dispatch@gohalohauling.com; honeypot spam protection; thank-you page.

### Other pages (content rules)
- Sizes & Pricing: size cards w/ dimensions + typical loads; price shows "Call for quote" until you give real numbers; weight limits / overage as TBD.
- C&D Debris: accepted materials, recycling/diversion approach, contractor focus.
- LEED Recycling Reports: what reports you provide (weight tickets, diversion %, facility names) — **only what you actually provide**.
- Green Halo Reporting Support: "we provide the tickets/data your project needs to submit in Green Halo"; no logo, no "partner/certified" wording; disclaimer.
- Service Areas: Bay Area, CA; city list left as placeholder until you confirm.
- Contact: emails, phone, Instagram, short form.

### SEO / basics
Per-page titles + meta descriptions, LocalBusiness schema, sitemap, Google Business Profile (recommend creating), image compression, fast load on phones.

## Repo structure
```
website/
  README.md            # how to edit, deploy, from any device
  docs/plan.md         # this plan
  docs/content-todo.md # facts you must confirm (prices, cities, phone, FAQ answers)
  src/pages/*.astro    # 7 pages
  src/components/      # Header, Footer, QuoteForm, SizeCard, FAQ
  src/styles/global.css
  public/images/       # logo + job photos
```

## Open items you must confirm (tracked in content-todo.md)
Phone number, cities served, prices/rental period/weight limits, which sizes you actually own, which services you really offer (dirt/concrete? LEED reports?), delivery lead time.

## Verification
- `npm run build` passes; preview locally and screenshot at phone + desktop widths (Playwright).
- Submit test quote → email arrives at dispatch@.
- Lighthouse mobile ≥90; check no Green Halo affiliation wording.
- Connect Cloudflare Pages to repo, point gohalohauling.com DNS, confirm HTTPS.
