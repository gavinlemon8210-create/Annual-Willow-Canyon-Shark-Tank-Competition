# Annual Willow Canyon Shark Tank Competition

## Project Overview
A static website for the Annual Willow Canyon Shark Tank Competition — a high school pitch competition where student teams present original product concepts to real-world finance professionals. The competition is run by the **Arizona Student Investment Council (ASIC)** at **Willow Canyon High School** in the **Dysart Unified School District**.

The live site is hosted at **wcsharktank.org** via **GitHub Pages**, deploying automatically from the `main` branch of this repository.

## Tech Stack
- **Pure static HTML/CSS/JS** — single `index.html` file, no build step, no framework
- **GitHub Pages** — auto-deploys on push to `main`
- **Custom domain** — wcsharktank.org
- **Fonts** — Google Fonts: Cormorant Garamond (serif, headings) + Inter (sans-serif, body)
- **Images** — stored in `/images/` directory (sponsor logos, etc.)

## Color Scheme
Navy and gold throughout. Key CSS variables and values:
- **Gold / Electric:** `#c3991a` / `rgba(195,154,41,...)` — borders, accents, badges
- **Bright gold:** `#d4aa3a`, `#e8cc7a`, `#f0d97a` — gradients, hero text shimmer
- **Ice / White:** `rgba(240,228,176,...)` — body text tones
- **Navy background:** deep navy `#0a1832` range with translucent overlays

Card hover effects use a gold shimmer sweep (`::before` pseudo-element). Section backgrounds alternate between slight navy tints.

## Site Structure (sections in order)
1. **Hero** — title, tagline, CTA buttons, event details (date, location, est. time)
2. **About** — what ASIC is, stat cards
3. **Qualifier Round Details** — timeline: create product → present → advance to finals
4. **Judging Criteria** (`#advance`) — four criteria cards (Realistic, Problem-Solving, Creative, Profitable) + link to full rubric. "Finals" nav link points here.
5. **Finals Format** (`#finals`) — numbered editorial steps (01–04)
6. **Curveball Questions** (`#curveballs`) — four possible finals questions
7. **Competition Prizes** (`#prizes`) — Chick-fil-A, Raising Cane's, Starbucks, Texas Roadhouse sponsor cards with logos
8. **Register** (`#register`) — registration form
9. **Contact** (`#contact`)

## Competition Details
- **Date:** May 7th
- **Location:** Willow Canyon Cafeteria
- **Est. Time:** 12:30 – 3:15
- **Format:** Teams of students present a 4–6 slide pitch (4 min presentation + 2 min Q&A). Top team per panel advances to finals.
- **Finals:** Teams answer 2 of 4 possible curveball questions, ~3 minutes each.
- **Prizes:** Gift card prize pool from Chick-fil-A, Raising Cane's ($200), Starbucks, and Texas Roadhouse (~$100) — 1st, 2nd, and 3rd place pick from the pool.

## Slideshow Requirements (qualifier)
Student presentations must cover:
- Function
- Problem Statement
- Visual Representation
- Limitations
- Competitive Advantages
- Production Cost Overview (estimated cost per unit + materials)

## Sponsor Logos
Stored in `/images/`:
- `chick-fil-a-logo.png`
- `raising-canes-logo.png`
- `starbucks-logo.png`
- `texas-roadhouse-logo.png`

## Deployment
Push to `main` → GitHub Pages builds and serves automatically. No CI, no build pipeline. Changes are live within ~1 minute of push.

## Key Design Patterns
- All cards share a gold shimmer hover via `.finals-card, .cq-card, .prize-card, .curveball-note` group selector
- Section labels (small gold uppercase text above headings) use `.section-label`
- The `#advance` section ID is what the "Finals" nav link targets — do not rename it without updating nav hrefs
- Mobile nav is a separate `#mobileNav` div; both desktop and mobile navs must be kept in sync when adding/removing links
