# NSA Travels — Website

**Nepal South Asia International Travels and Tours Pvt. Ltd.**

A fully static, pre-built React + Vite travel agency website. There are no source files — all application code lives in the compiled bundle. To make changes, edit the minified JS directly.

---

## Quick Start

Serve the site locally using Node.js (no install required):

```bash
npx --yes serve . -p 3000
```

Then open [http://localhost:3000](http://localhost:3000) in your browser.

> **Requirements:** Node.js (v14+). Python is **not** available in this environment.

---

## Project Structure

```
agent/
│
├── index.html                          # Entry point — loads the JS + CSS bundles
├── logo.png                            # Site logo
├── README.md                           # This file
│
├── assets/
│   ├── index-B9htVR2e.js              # Entire compiled React app (minified)
│   └── index-i7-0ZTJ0.css             # All site styles (minified)
│
└── images/
    ├── hero/
    │   ├── hero-bg.jpg                 # Homepage hero background image
    │   ├── flights-hero.jpg            # Flight Tickets page hero
    │   ├── hotels-hero.jpg             # Hotels page hero
    │   ├── tours-hero.jpg              # Tour Packages page hero
    │   ├── trekking-hero.jpg           # Trekking page hero
    │   ├── helicopter-hero.jpg         # Chopper / Helicopter page hero
    │   └── vehicles-hero.jpg           # Vehicles page hero
    │
    ├── destinations/                   # Destination images
    │   │                               # — 7 main destinations use dual variants:
    │   │                               #     <slug>-card.jpg  → shown on cards & grids
    │   │                               #     <slug>-hero.jpg  → shown on detail page hero
    │   ├── thailand-card.jpg
    │   ├── thailand-hero.jpg
    │   ├── malaysia-card.jpg
    │   ├── malaysia-hero.jpg
    │   ├── vietnam-card.jpg
    │   ├── vietnam-hero.jpg
    │   ├── bali-card.jpg
    │   ├── bali-hero.jpg
    │   ├── singapore-card.jpg
    │   ├── singapore-hero.jpg
    │   ├── dubai-card.jpg
    │   ├── dubai-hero.jpg
    │   ├── maldives-card.jpg
    │   ├── maldives-hero.jpg
    │   │                               # — legacy single images (other destinations):
    │   ├── australia.jpg
    │   ├── austria.jpg
    │   ├── azerbaijan.jpg
    │   ├── bhutan.jpg
    │   ├── cambodia.jpg
    │   ├── china.jpg
    │   ├── czech-republic.jpg
    │   ├── france.jpg
    │   ├── germany.jpg
    │   ├── hongkong.jpg
    │   ├── india.jpg
    │   ├── italy.jpg
    │   ├── japan.jpg
    │   ├── jordan.jpg
    │   ├── mauritius.jpg
    │   ├── netherlands.jpg
    │   ├── newzealand.jpg
    │   ├── qatar.jpg
    │   ├── saudi-arabia.jpg
    │   ├── seychelles.jpg
    │   ├── south-africa.jpg
    │   ├── southkorea.jpg
    │   ├── spain.jpg
    │   ├── srilanka.jpg
    │   ├── switzerland.jpg
    │   ├── turkey.jpg
    │   └── united-kingdom.jpg
    │
    ├── nepal/                          # Nepal-specific destination images
    │   ├── chitwan.jpg
    │   ├── everest.jpg
    │   ├── kathmandu.jpg
    │   ├── pokhara.jpg
    │   └── trekking.jpg
    │
    ├── packages/                       # Tour package category images
    │   ├── adventure.jpg
    │   ├── family.jpg
    │   └── honeymoon.jpg
    │
    └── partners/                       # Partner & certification logos (marquee section)
        ├── airlines/                   # Airline partner logos
        │   ├── nepal-airlines.png
        │   ├── buddha-air.png
        │   ├── yeti-airlines.png
        │   ├── qatar-airways.png
        │   ├── emirates.png
        │   ├── thai-airways.png
        │   ├── singapore-airlines.png
        │   ├── air-india.png
        │   ├── malaysia-airlines.png
        │   ├── flydubai.png
        │   └── cathay-pacific.png
        │
        ├── hotels/                     # Hotel partner logos
        │   ├── hyatt.png
        │   ├── marriott.png
        │   ├── hilton.png
        │   ├── sheraton.png
        │   ├── radisson.png
        │   ├── taj.png
        │   ├── oberoi.png
        │   └── leela.png
        │
        ├── payments/                   # Payment partner logos
        │   ├── esewa.png
        │   ├── khalti.png
        │   ├── imepay.png
        │   ├── neppay.png
        │   ├── connectips.png
        │   ├── fonepay.png
        │   ├── visa.png
        │   └── mastercard.png
        │
        └── certifications/             # Authorized & Certified By logos
            ├── iata.png
            ├── natta.png
            ├── taan.png
            ├── ntb.png
            └── nrb.png
```

---

## Pages & Routes

| Route | Page |
|---|---|
| `/` | Home |
| `/destinations` | Destinations |
| `/packages` | Packages |
| `/nepal` | Nepal Tours |
| `/about` | About Us |
| `/contact` | Contact |
| `/visa` | Visa Services |
| `/insurance` | Travel Insurance |
| `/events` | Events & Activities |
| `/sitemap` | Sitemap |
| `/blog` | ~~Blog~~ → redirects to `/` (removed) |

---

## Partner Logos — How to Add

The partner marquee component automatically displays a logo image if the file exists, or falls back to a letter placeholder if the file is missing. Simply drop the correctly named PNG into the right folder:

| Section | Folder |
|---|---|
| Airline Partners | `images/partners/airlines/` |
| Hotel Partners | `images/partners/hotels/` |
| Payment Partners | `images/partners/payments/` |
| Authorized & Certified By | `images/partners/certifications/` |

**Recommended format:** PNG with transparent background, min 200×80px.  
Files **must match the exact filenames** listed in the project structure above.

---

## Making Changes

Since this is a pre-built static site (no source code), all edits are made directly to the compiled bundle:

**File to edit:** `assets/index-B9htVR2e.js`

### Key locations inside the bundle

| What | Variable | Line |
|---|---|---|
| Navigation menu links | `Q1` | ~19 |
| Footer company links | `A8` | ~24 |
| Airline partner data | `ZA` | ~75 |
| Hotel partner data | `JA` | ~75 |
| Payment partner data | `eE` | ~75 |
| Certification data | `tE` | ~75 |
| Destination cards array | `jv` | ~75 |
| Flight route cards array | `IA` | ~75 |
| Destination detail page data | `tD` | ~84 |
| Sitemap page content | `xD` | ~75 |
| App routes | — | ~84 |

> **Tip:** Use VS Code's Find (`Ctrl+F`) on the JS file to locate the variable name, then edit the surrounding JSON-like object array.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 18 |
| Build Tool | Vite |
| Routing | React Router |
| Styling | CSS (compiled) |
| Deployment | Static file server (any) |

---

## Deployment

This is a fully static site — no backend, no build step required. Deploy by copying all files to any static host:

- **Vercel / Netlify:** Drag and drop the `agent/` folder
- **cPanel / FTP:** Upload all files to `public_html/`
- **GitHub Pages:** Push to a repo with Pages enabled
- **Local:** `npx serve . -p 3000`

> Make sure the server serves `index.html` for all routes (SPA fallback) so React Router works correctly on direct URL access.
