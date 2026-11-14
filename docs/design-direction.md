# Design Direction (taste-skill pass)

Planning only. Nothing here is built yet. Produced with the taste-skill design rules (v2.5.1) against [plan.md](plan.md) and [instagram-review.md](instagram-review.md).

## 1. What kind of site this is
**Service (a trade).** People hire Halo Hauling. The skill treats that as: real photographs lead, flat colour, type, no flashy effects, one or two quiet photo-led "moments".

- **What's sold:** roll-off dumpster rental and debris hauling
- **Who buys:** contractors first, then homeowners and businesses
- **One main action, worded the same everywhere:** **Get a quote** (nav, hero, closing section, phone bar)

## 2. The look (dealt by the skill, adjusted to your brand)
| Part | Choice | Why |
|---|---|---|
| Colours | **Your chosen palette** (see §2a) | Your palette, reference: [reference/brand/palette.png](reference/brand/palette.png). The only blue on the site is your real dumpsters in the photos, so they pop against the greens. |
| Type | **Newsreader** (serif headings) + **Hanken Grotesk** (body), both free Google Fonts | Skill dealt a slab font first; switched to its serif option because your Instagram posts already use an elegant serif ("Find Your *Perfect Fit.*"). |
| Corners | Soft | Default for a service |
| Hero | ✅ **Split (half-width), owner's choice:** text on the left (5 of 12 columns), photo on the right (628×716, rounded corners), both fully on the first screen. One small flat card on the photo's lower-left with a hard fact ("10 to 40 yards · hook-lift delivery"). On phones: text first, photo under it. | Works with the ~1,450px photos (shown at 628px, so sharp on retina). The truck/A28 photo is near-square, so it fits the tall frame. |
| Nav | Centred links, logo left, "Get a quote" button right; full-screen menu on phones; sticky quote/call bar at the bottom on phones | |
| Buttons | Tonal (soft filled) | |
| Rhythm | One band of 1–2 sections on the darker cream surface | Separates the contractor/documentation part |
| Closing | Big photo of your yard/dumpsters with "Get a quote" | |
| Footer | Dark forest green | Matches logo |
| Logo | Your logo set (see §2b) replaces the skill's mark | |
| Motion | Hero fades in once on load; buttons and photo cards respond on hover. **Two moments:** "photo chapters" (how it works, photos change as you scroll) and "picture develops" (one job photo fades in like a print). No carousels, no parallax, nothing that blinks. | |

### 2a. Palette (owner's choice)
| Name | Hex | Role on the site |
|---|---|---|
| Cream | `#F3EAE0` | Page background; text on dark sections |
| Forest | `#233B2C` | Main text, header, footer, dark band |
| Olive | `#35442F` | **Buttons** ("Get a quote") with cream text |
| Sage | `#A5AC8B` | Soft accents on dark sections, icon backgrounds, size-card tags |
| Gold | `#C6A66B` | Thin divider lines, logo, small highlights **on dark green only** |
| (derived) Sand | `#E8DECF` | Card/band surface, a shade darker than cream |
| (derived) Muted | `#5A6352` | Secondary text |

Contrast checked (WCAG; 4.5 needed for text):
- ✅ Forest on cream 10.2 · olive on cream 8.7 · cream on forest 10.2 · gold on forest 5.2 · sage on forest 5.1
- ❌ **Gold or sage text on cream = 2.0.** Too faint to read, so on light backgrounds these are only used for lines and shapes, never for words.
- Validated with taste-skill's `start.mjs brand` (accepted).

### 2b. Logo set ([reference/brand/logo-options.webp](reference/brand/logo-options.webp))
| Version | Use |
|---|---|
| Winged-H mark | Header (about 40px tall), favicon, phone home-screen icon |
| Round badge (HALO HAULING) | Footer, Instagram/Google profile, share image, truck/shirts |
| Horizontal wordmark with truck | Closing section or share image only. Too detailed for the header; truck and trees disappear at small sizes. |

✅ **Logo files received** (transparent background), split into web-ready PNGs in [reference/brand/](reference/brand/):
- `logo-mark-winged-h.png` (439×313): header, next to "HALO HAULING" set in the heading font
- `logo-badge-round.png` (397×397): footer, favicon source, social profile, share image
- `logo-wordmark-truck.png` (1193×531): closing section / share image only
- Tested on Cream and Forest: all three read well on both. The winged-H still reads at 48px; for the browser-tab favicon (16–32px) use the round badge or a simplified H.
- Still nice to have later: an SVG version from the designer for perfectly sharp edges.

## 3. Voice
**Facts only, trade words.** Short, plain sentences with real nouns: yards, tons, driveway, swap, weight ticket, hook-lift. "You" for the customer, "we" for the work.
- No "premium / seamless / elevate", no invented stats, no fake reviews.
- Example tone: "We drop a 20-yard box in your driveway on boards, you fill it, we swap or haul it when you call."
- Proof only when real: a customer quote with permission, a Google review count later.

## 4. Home page, screen by screen (1440×900 desktop)
| # | Section | One idea | Picture | Screens |
|---|---|---|---|---|
| 1 | Hero | Bay Area roll-off dumpsters, quote in one click | Truck with A28 + Halo mud flap | 1 |
| 2 | Services | 5 services, one line each (roll-off rentals, C&D debris, dirt & concrete, cleanouts, hauling & disposal) + "one box or several, one-time or ongoing" | Warehouse dock with 3 boxes (real) | 1 |
| 3 | Sizes — *Find your perfect fit* | 10 / 15 / 20 / 30 / 40 yd (or your real sizes), best use, "price on request" | Size list (allowed picture-less) | 1 |
| 4 | How it works (**photo-chapters moment**) | Tell us (in the intro line) → we drop it → you fill it → we haul it | 3 photos, one per chapter | 3 (scroll) |
| 5 | Contractors *(dark forest band)* | Swaps on schedule, multiple boxes per job, weight tickets on request. LEED/Green Halo added here **later** | Loaded dumpster on a job site (**picture-develops moment**) | 1 |
| 6 | Service area | Bay Area, the cities you confirm | Still map of the South Bay/Bay Area with your cities | 1 |
| 7 | FAQ | 5 questions | none (allowed) | 1 |
| 8 | Quote form | size, material, delivery address, date, + "Prefer to talk? Instagram @halohauling" | A12 driveway drop (real) beside form | 1–2 |
| 9 | Closing + footer | Get a quote | Tall C&D box, open lot | 1 |

"Who it's for" (homeowners / contractors / businesses) is folded into Services instead of its own section. The skill says short blocks get merged.

**Inner pages** (Sizes & Pricing, C&D Debris, LEED Reports, Green Halo Support, Service Areas, Contact) use the same system, 2–4 sections each: photo hero → details → quote form.

## 5. Where the skill and your plan disagree (my calls)
| Skill says | Your business needs | Decision |
|---|---|---|
| One single page, all links to sections | 7 pages (better for Google searches like "LEED recycling reports San Jose") | **Keep 7 pages.** Home follows the skill's story; inner pages are short. |
| Fake `.example` emails, no real phone | Real contact details | **Use real** `@gohalohauling.com` emails and phone. |
| Fill missing photos with licensed stand-ins | "Real photos only" | **Real photos only.** See shot list below; build waits for them. |
| h1 max ~32 characters | Requested headline "Roll-Off Dumpster Rentals & Construction Debris Solutions" (56) | ✅ **Approved:** h1 "Bay Area roll-off dumpsters", your full headline as the line under it. HALO HAULING stays in the logo/nav. The "C&D Recycling • LEED Documentation • Green Halo Reporting Support" line is held until those services are ready (see §5a). |
| No captions under images | — | Fine, follow it. |
| AI-made images are not real work | 3 of 6 Instagram posts are designed graphics | Not used as photos on the site. |

### 5a. Launch now vs. later (owner: "Yes, but later — no certificates yet")
Recycling, LEED reports and Green Halo support are planned but **not ready**, so the site shouldn't advertise them yet.
- **Launch (phase 1), 5 pages:** Home · Dumpster Sizes & Pricing · Construction & Demolition Debris · Service Areas · Contact
- **Phase 2 (when you can provide the paperwork):** add LEED Recycling Reports + Green Halo Reporting Support pages, the "C&D Recycling • LEED Documentation • Green Halo Reporting Support" line, and the documentation question on the quote form. The pages are designed now so adding them later is a small change.
- Sizes confirmed: **10, 15, 20, 30, 40 yards.**

## 6. Photographs (9 received, in [reference/photos/](reference/photos/))

### 6a. Where each photo goes (home page)
| Slot | Photo | Why |
|---|---|---|
| Hero (split, right half) | `ig-a28-truck-logo-mudflap` | Your truck with the **Halo Hauling mud-flap logo**; near-square, fits the tall frame |
| Services | `ig-warehouse-dock` | 3 boxes at a loading dock: shows commercial/business service |
| Sizes: *Find your perfect fit* | `residential-dumpster-rental` (tall portrait) beside the size list | Tall box at the curb, golden light |
| How it works (photo-chapters) 1. We drop it | `ig-a12-driveway-swaploader` | Hook-lift setting a box in a driveway, boards under the rollers |
| 2. You fill it | `concrete-debris-removal` | Box full of broken concrete in a driveway |
| 3. We haul it | `dumpster-delivery-pickup` | Truck at the curb with a C&D box, fenced job site |
| Contractors band (picture-develops) | `dirt-removal-hauling` | Two boxes of dirt on one job with cones: matches your "multiple dumpsters, one job" post |
| Quote form | `quote-low-sided-dumpster` | Low-sided box at a house, empty and ready |
| Closing | `hero-dumpster` | Tall C&D box in an open lot, wide sky (after the sticker fix below) |

Inner pages reuse these: Sizes → hero-dumpster + quote-low-sided; C&D → concrete + dumpster-delivery-pickup; Service Areas → residential-dumpster-rental; Contact → ig-a12-driveway.

### 6b. Fixes needed before they go on the site
1. ✅ **Stickers removed** (owner confirmed these are Halo boxes): the "RENT ME" sticker on `hero-dumpster` and the "KELLY" sticker on `dumpster-delivery-pickup` are retouched out. Originals stay in git history.
2. ✅ **All 9 confirmed real** Halo Hauling equipment and jobs (owner).
3. ✅ **Size:** no originals, so the plan uses the **half-width split hero**. Full-width uses (how-it-works chapters, closing photo) stay at about 1,450px: fine on normal screens, slightly soft on large retina displays. Original phone files can replace them any time with no design change.
4. ✅ **Logo received**, see §2b.
5. All photos are reused only once per page (skill rule: no photo twice).

### 6c. Still useful later
- A box being loaded on a job, you two with the truck (only if you want to be on the site), a weight ticket (blurred) for phase 2 LEED/Green Halo pages.

## 7. Facts still empty (the skill won't invent them)
Phone · cities · prices or "on request" · rental period · weight limits · delivery lead time · ongoing service for businesses (yes/no now?). Tracked in [content-todo.md](content-todo.md).

## 8. Checks we'll run when building
The skill's own checker in a real browser at 1440, 1024, 820, 768, 390 and 320 px: layout edges, one section per screen, contrast, tap sizes, form labels, copy check (no filler words), and page speed.
