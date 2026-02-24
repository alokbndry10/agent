# NSA Travels — Website

**Nepal South Asia International Travels and Tours Pvt. Ltd.**

Live site: [https://nepalsouthasiatravels.com.np](https://nepalsouthasiatravels.com.np)

A fully static, pre-built React + Vite travel agency website. There are no source files — all application code lives in the compiled bundle. To make changes, edit the minified JS directly.

---

## Quick Start

Serve the site locally using Node.js (no install required):

```bash
npx --yes serve . -p 3000
```

Then open [http://localhost:3000](http://localhost:3000) in your browser.

> **Requirements:** Node.js (v14+).

---

## Project Structure

```
agent/
│
├── index.html                          # Entry point — SEO meta tags, JSON-LD schema
├── logo.png                            # Site logo
├── sitemap.xml                         # XML sitemap (all 20 pages, submitted to GSC)
├── robots.txt                          # Search engine crawl rules
├── vercel.json                         # SPA rewrite rules + static file exclusions
├── googlee769bec0be0e47e4.html         # Google Search Console ownership verification
├── server.js                           # Local dev server (port 3000)
├── package.json
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
    ├── nepal/                          # Nepal destination images
    │   ├── chitwan.jpg
    │   ├── everest.jpg
    │   ├── kathmandu.jpg
    │   ├── pokhara.jpg
    │   └── trekking.jpg
    │
    ├── trekking/                       # Trekking page images
    │   ├── everest-base-camp.jpg
    │   ├── annapurna-circuit.jpg
    │   ├── poon-hill.jpg
    │   ├── manaslu-circuit.jpg
    │   ├── gokyo-lakes.jpg
    │   └── langtang-valley.jpg
    │
    ├── blog/                           # Blog page images
    │   ├── bali.jpg
    │   ├── everest.jpg
    │   ├── malaysia-visa.jpg
    │   ├── nepal-airlines.jpg
    │   ├── thailand.jpg
    │   └── vietnam.jpg
    │
    ├── vehicles/                       # Vehicles page images
    │   ├── sedan.jpg
    │   ├── suv.jpg
    │   ├── hiace.jpg
    │   └── coaster.jpg
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

| Route | Page | Sitemap Priority |
|---|---|---|
| `/` | Home | 1.0 |
| `/visa-services` | Visa Services | 0.9 |
| `/flight-tickets` | Flight Tickets | 0.9 |
| `/tour-packages` | Tour Packages | 0.9 |
| `/destinations` | Destinations | 0.8 |
| `/nepal-dmc` | Nepal DMC | 0.8 |
| `/trekking` | Trekking | 0.8 |
| `/hotels` | Hotels | 0.7 |
| `/packages` | Packages | 0.7 |
| `/blog` | Blog | 0.7 |
| `/nepal` | Nepal Tours | 0.6 |
| `/helicopter` | Helicopter / Chopper | 0.6 |
| `/vehicles` | Vehicles | 0.6 |
| `/insurance` | Travel Insurance | 0.6 |
| `/events` | Events & Activities | 0.6 |
| `/about` | About Us | 0.5 |
| `/contact` | Contact | 0.5 |
| `/sitemap` | Sitemap | 0.5 |
| `/terms` | Terms & Conditions | 0.3 |
| `/privacy` | Privacy Policy | 0.3 |

---

## SEO

| Item | Status |
|---|---|
| `sitemap.xml` | ✅ Live, submitted to Google Search Console |
| `robots.txt` | ✅ Allows all crawlers, points to sitemap |
| Canonical tag | ✅ `https://nepalsouthasiatravels.com.np/` |
| Open Graph tags | ✅ Correct domain, absolute image URLs |
| Twitter Card tags | ✅ |
| JSON-LD schema | ✅ TravelAgency type with address, geo, phone, hours |
| Google Search Console | ✅ Verified (HTML file method) |

> **Note:** All 20 pages share the same `<title>` and `<meta description>` from `index.html` because this is a pre-built SPA with no source code. Per-page meta tags would require rebuilding the bundle with `react-helmet`.

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
| Carousel animation | Pure CSS `@keyframes` (GPU-composited) |
| Deployment | Vercel |

---

## Deployment

Deployed on **Vercel** via GitHub (`alokbndry10/agent`, `main` branch). Every `git push` to `main` auto-deploys.

`vercel.json` contains a SPA catch-all rewrite that serves `index.html` for all routes except static assets, `sitemap.xml`, `robots.txt`, and the Google verification file.

For other hosts:
- **Netlify:** Drag and drop the folder, add a `_redirects` file: `/* /index.html 200`
- **cPanel / FTP:** Upload all files to `public_html/`, configure `.htaccess` for SPA fallback
- **Local:** `npx serve . -p 3000`
