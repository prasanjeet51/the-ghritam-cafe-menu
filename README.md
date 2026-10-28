# The Ghritam Cafe — Digital Menu & Direct Ordering

A searchable digital menu for a real, family-run cafe in Mithanpura, Muzaffarpur, Bihar — built to reduce dependence on delivery platforms that take around 33% commission.

**Live customer site (Netlify):** https://precious-mochi-ed2190.netlify.app
**GitHub Pages (after you publish this repo):** `https://prasanjeet51.github.io/the-ghritam-cafe-menu/`

## The problem

In a price-sensitive market, raising menu prices cuts footfall, and discounting burns cash with no guarantee of profit. The cafe was losing roughly a third of each delivery-platform order to commission, while its own counter prices were far lower — for example, a Maharaja burger is ₹110 at the counter vs ₹219 on Swiggy.

## What this site does

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

- Single self-contained file: `index.html` (HTML + CSS + JavaScript, no build step, no framework)
- No backend, no database in this version
- Deployed for customers on Netlify; this repo is the portfolio/source copy, publishable on GitHub Pages

## Run it locally

Open `index.html` in any browser. No server, install, or build step is needed.


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
