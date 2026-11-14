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
| Hero | **Full-bleed photo** with the words in a solid cream box on the calm side (sky) | Truck-with-A28 photo has a big clear sky. No dark overlays or gradients. |
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

**Logo files needed for the web:** the current logos are images with a dark green background baked in, and that green doesn't quite match Forest `#233B2C`, so a box edge would show. Ask your designer for:
1. **Transparent PNG** (or better, **SVG**) of each version
2. A **one-colour** version of the winged-H (gold or cream) for small sizes and the favicon. The 3D shine turns to mush under 48px.

If you can't get those, I can cut out the background, but the result is lower quality.

## 3. Voice
**Facts only, trade words.** Short, plain sentences with real nouns: yards, tons, driveway, swap, weight ticket, hook-lift. "You" for the customer, "we" for the work.
- No "premium / seamless / elevate", no invented stats, no fake reviews.
- Example tone: "We drop a 20-yard box in your driveway on boards, you fill it, we swap or haul it when you call."
- Proof only when real: a customer quote with permission, a Google review count later.

## 4. Home page, screen by screen (1440×900 desktop)
| # | Section | One idea | Picture | Screens |
|---|---|---|---|---|
| 1 | Hero | Bay Area roll-off dumpsters, quote in one click | Truck carrying A28 (real) | 1 |
| 2 | Services | 5 services, one line each (roll-off rentals, C&D debris, dirt & concrete, cleanouts, hauling & disposal) + "one box or several, one-time or ongoing" | Warehouse dock with 3 boxes (real) | 1 |
| 3 | Sizes — *Find your perfect fit* | 10 / 15 / 20 / 30 / 40 yd (or your real sizes), best use, "price on request" | Size list (allowed picture-less) | 1 |
| 4 | How it works (**photo-chapters moment**) | 4 steps: tell us → we drop it → you fill it → we haul it | 4 real photos, one per step | 3 (scroll) |
| 5 | Contractors *(dark forest band)* | Swaps on schedule, multiple boxes per job, weight tickets on request. LEED/Green Halo added here **later** | Loaded dumpster on a job site (**picture-develops moment**) | 1 |
| 6 | Service area | Bay Area, the cities you confirm | Still map of the South Bay/Bay Area with your cities | 1 |
| 7 | FAQ | 5 questions | none (allowed) | 1 |
| 8 | Quote form | size, material, delivery address, date, + "Prefer to talk? Instagram @halohauling" | A12 driveway drop (real) beside form | 1–2 |
| 9 | Closing + footer | Get a quote | Your yard / row of boxes | 1 |

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

## 6. Photographs
**Status:** owner has 9 photos + logo in a Mac folder "HaloHauling Web Images". Not yet in the repo. They'll be checked against the slots below once uploaded.

The skill wants **1–2 real photos per screen**; the home page needs **about 9 different ones** and no photo used twice. You have **3** usable (truck A28, driveway A12, warehouse dock). Shot list for phone photos (landscape, daylight, no customer faces or house numbers, wipe the boxes first):

1. Row of empty boxes, each size, in your yard (sizes section / closing)
2. Customer call / you at the truck with a tablet or phone (step 1)
3. Hook-lift setting a box down on boards in a driveway (step 2)
4. Box being loaded with debris on a real job (step 3)
5. Truck pulling away with a full box (step 4)
6. Full C&D box on a construction site (contractor band)
7. Close-up of a weight ticket / recycling receipt, customer info blurred (documentation)
8. Dirt or concrete load (dirt & concrete service)
9. Optional: you two with the truck (an "about us" line, only if you want to be on the site)

Also need: **original logo file** (PNG/SVG) and full-size originals of the 3 existing photos.

## 7. Facts still empty (the skill won't invent them)
Phone · cities · prices or "on request" · rental period · weight limits · delivery lead time · ongoing service for businesses (yes/no now?). Tracked in [content-todo.md](content-todo.md).

## 8. Checks we'll run when building
The skill's own checker in a real browser at 1440, 1024, 820, 768, 390 and 320 px: layout edges, one section per screen, contrast, tap sizes, form labels, copy check (no filler words), and page speed.
