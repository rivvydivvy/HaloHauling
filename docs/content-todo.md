# Content To Confirm Before Launch

Edit most of these in `src/site.ts`. Search the code for `TODO` to find the rest.

## Business info
- [ ] Business phone number (`site.phone`) — turns on Call buttons
- [ ] Domain decision: site + emails use **gohalohauling.com** (change in `src/site.ts` if different)
- [ ] Set up Google Workspace: info@, dispatch@, billing@ (dispatch/billing can be aliases at first)
- [ ] Web3Forms access key (`site.formKey`) — free at web3forms.com, register with dispatch@ email

## Services (only list what you actually provide)
- [ ] Confirm: Roll-off rentals, C&D debris, Dirt & concrete, Residential & commercial cleanouts
- [x] Sizes: 10 / 15 / 20 / 30 / 40 yd (confirmed)
- [ ] Dimensions per size (`sizes[].dims`)
- [ ] Prices, or keep "request a quote" (`sizes[].price`)
- [ ] Weight limits / overage fees, rental period, extension fee
- [ ] Prohibited items list (check with your disposal facility)

## LEED / Green Halo — PHASE 2 (owner: yes, later; no certificates yet)
- [ ] What LEED documentation you actually provide (weight tickets? diversion %? PDF summary?)
- [ ] Do you upload tickets into Green Halo for customers, or only supply them?
- [ ] Facilities you haul to (for diversion claims)

## Service area
- [ ] Exact cities served (`site.cities`)

## FAQ answers (src/pages/index.astro)
- [ ] How long can I keep it?
- [ ] Driveway protection
- [ ] Delivery lead time

## Photos & logo (put in `public/images/`)
- [x] Logo: transparent PNGs received (docs/reference/brand/). SVG optional later.
- [x] 9 real photos received and assigned (docs/reference/photos/, see design-direction.md §6)

## Launch
- [ ] Connect repo to Cloudflare Pages (build: `npm run build`, output: `dist`)
- [ ] Point gohalohauling.com DNS to Cloudflare Pages
- [ ] Create a Google Business Profile, link the site
- [ ] Add website link to Instagram bio
