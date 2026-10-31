# The Ghritam Cafe — Digital Menu & Direct Ordering

## v6 restyle (2026-10-31) — Emergent-inspired design pass
Same site, same data, new dress. Presentation-layer-only reskin of v5:
- Palette → warm cream (#FAF5EC) pages, chocolate-brown (#3B2A1E) headings/text, gold (#C9A227) CTAs and highlights
- Typography → Playfair Display serif headings (Google Fonts, graceful Georgia fallback offline), Jost clean sans body
- Gold primary pill buttons (Order Online, ADD+, View Cart, Call) + outlined secondary buttons, cream cards with hairline gold borders, leaf-ornament dividers under section headings
- Untouched: all 105 menu items, prices, names, PHOTOS map, cart logic, WhatsApp prefill, tel: intercept + call panel, review badge wording, search/filter, all JavaScript, all photos. Brand stays "The Ghritam Cafe".
- Preview screenshots in `preview/` (desktop index, desktop menu, cart view, mobile menu).

---

A searchable digital menu for a real, family-run cafe in Mithanpura, Muzaffarpur, Bihar — built to reduce dependence on delivery platforms that take around 33% commission.

**Live customer site (Netlify):** https://precious-mochi-ed2190.netlify.app
**GitHub Pages (after you publish this repo):** `https://prasanjeet51.github.io/the-ghritam-cafe-menu/`

## Changelog

- **2026-10-29 — Homepage (major):** the site is now two pages. `index.html` is a new animated homepage built from the cafe's own photos — real night storefront hero, real interior ambience, correctly labelled counter photos, logo lockup (THE / Ghritam / CAFÉ & RESTRO), How It Works, Today's Special, feature strip, and the full Mithanpura footer with address, directions, phone, and Instagram. `menu.html` is the clean menu-only page reached from Order Online — no repeated intro or footer, just Back to Home, the hours badge, and the full 105-item menu with search, cart, and WhatsApp ordering. Animation is lightweight CSS + scroll-reveal, with a reduced-motion fallback. Today's Special dish photos are still needed (pasta / loaded fries / shake) — those cards currently carry a photo-needed note rather than another dish's photo.
- **2026-10-28 —** Menu live on Netlify and GitHub Pages (105 items, counter prices).

## The problem

In a price-sensitive market, raising menu prices cuts footfall, and discounting burns cash with no guarantee of profit. The cafe was losing roughly a third of each delivery-platform order to commission, while its own counter prices were far lower — for example, a Maharaja burger is ₹110 at the counter vs ₹219 on Swiggy.

## What this site does

- **Two pages:** an animated homepage (`index.html`) with the cafe's real photos, and a clean menu-only page (`menu.html`) reached from Order Online
- **105 items across 14 categories**, at counter prices (not platform markups)
- Search, category chips, and a Bestsellers row (12 items)
- Veg-only toggle
- Mobile cart with totals, opening as a full-screen view
- **"Place Order on WhatsApp"** — opens WhatsApp with the order text prefilled to the cafe number (9069003133)
- Cafe address (Mithanpura, Muzaffarpur, Bihar 842002) and hours (10:30 AM – 11:30 PM, daily), with a live open/closed badge
- Restaurant + Menu structured data for search indexing

## What it does NOT do yet (honest scope)

- This is a menu + WhatsApp order handoff, **not** a full automated ordering backend. There is no payment integration, no automatic delivery booking, and no order tracking in this version yet.
- No footfall or revenue uplift is claimed — those have not been measured yet.
- Direct orders are prepaid-only by policy; cash on delivery stays on Swiggy/Zomato, where the platforms collect and guarantee payment.

Planned next step (Step 2): location → distance-based delivery slab → bill → custom per-order UPI link → payment confirmation → one-tap Rapido booking preparation.

## Tech

- Two self-contained files: `index.html` (homepage, photos embedded) and `menu.html` (menu + WhatsApp cart, HTML + CSS + JavaScript, no build step, no framework)
- No backend, no database in this version
- Deployed for customers on Netlify; this repo is the portfolio/source copy, publishable on GitHub Pages

## Run it locally

Open `index.html` in any browser, with `menu.html` in the same folder so Order Online works. No server, install, or build step is needed.

## Publish on GitHub Pages

1. Create a public repo named `the-ghritam-cafe-menu` and upload `index.html` + this `README.md` to the `main` branch.
2. In the repo: Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save.
3. Your live link will be `https://prasanjeet51.github.io/the-ghritam-cafe-menu/`

## How it was built and tested

- Menu data taken from the cafe's physical menu card (counter prices), cross-checked against its Swiggy listing.
- Tested on a phone: search, category chips, veg toggle, cart totals, and the WhatsApp order handoff.
- Two real bugs found in testing were fixed before shipping: a cart that half-rendered as a bottom sheet (replaced with a full-screen cart view), and a phone-number button that opened a viewer instead of the dialer on some in-app browsers.

Built with AI-assisted development — I led the problem definition, business rules (counter pricing, prepaid-only, delivery slabs), testing, and deployment decisions.

## Project facts

- Cafe: THE GHRITAM CAFE, Mithanpura, Muzaffarpur, Bihar
- Phone / WhatsApp for orders: 9069003133
- Instagram: @the_ghritam
- Hours: 10:30 AM – 11:30 PM, daily

## Changelog — 2026-10-29 (v5 restyle)

- Elegant restyle of both pages (reverse-engineered cues from a local
  competitor's site, rebuilt with the cafe's own real content — no stock
  photos, no fake counters).
- Menu page: dish photos on cards, keyed by EXACT menu item name so the
  brother's future photos drop in by name (see the "DISH PHOTOS" comment in
  menu.html). Items without a photo get an elegant monogram tile — nothing
  looks broken or mislabelled. 5 real photos wired: Latte, Freshly Baked
  Nachos, Classic Cold Coffee, Hot Coffee, Cappuccino.
- Both pages: "⭐ 5.0 · 23 Google reviews" badge (real rating) linking to the
  Mithanpura listing.
- Homepage contact fix: the footer number is now a big Call button; tapping
  tries the dialer directly and falls back to a call panel (copy number /
  WhatsApp) if the in-app viewer swallows the tel: hand-off.
- Upload: replace index.html, menu.html and README.md in
  prasanjeet51/the-ghritam-cafe-menu, wait 1–2 min, verify both URLs.
