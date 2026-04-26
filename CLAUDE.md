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
4. **Judging Criteria** (`#advance`) — three criteria cards (Creativity, Problem-Solving, Target Market) + link to full rubric. "Finals" nav link points here.
5. **Finals Format** (`#finals`) — numbered editorial steps (01–05)
6. **Curveball Questions** (`#curveballs`) — four possible finals questions
7. **Competition Prizes** (`#prizes`) — Chick-fil-A, Raising Cane's, Starbucks, Texas Roadhouse sponsor cards with logos
8. **Register** (`#register`) — registration form
9. **Contact** (`#contact`)

## Competition Details
- **Date:** May 7th
- **Location:** Willow Canyon Cafeteria
- **Est. Time:** 12:30 – 3:15
- **Format:** Teams of students present a 4–6 slide pitch (5 min presentation + 1 min Q&A). Top team per panel advances to finals.
- **Finals:** Teams answer 2 of 4 possible curveball questions, ~3 minutes each.
- **Prizes:** Gift card prize pool from Chick-fil-A, Raising Cane's ($200), Starbucks, and Texas Roadhouse (~$100) — 1st, 2nd, and 3rd place pick from the pool.

## Slideshow Requirements (qualifier)
Student presentations must cover (aligned with rubric categories):
- Function — what your product does
- Problem Statement — the problem it solves
- Target Market — who your customers are
- Visual Representation — drawing, diagram, 3D model, or physical model (worth 10 automatic rubric points if present)
- Limitations — honest about inefficiencies and structural constraints
- Competitive Advantages — why your product beats current substitutes

**Production Cost Overview has been intentionally removed** from requirements. Profitability is no longer a standalone judging category per the updated rubric.

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

## Judging Rubric

The rubric was updated to focus on **creativity, problem-solving, and target market** — profitability and production costs are **not** a standalone judging category. The site should emphasize creativity and presentation skills, which carry the most weight. Do not re-introduce profitability/cost emphasis.

### Qualifier Rubric (67 pts total)

**1. Creativity (30 pts) — Highest weighted category (~45% of total score)**
- a. Originality (10 pts): Copycat (0–3 pts) | Similar to existing products (4–6 pts) | Completely unique/novel concept (7–10 pts)
- b. Presentation Clarity/Features (10 pts): Confusing, barely conveys product (0–3 pts) | Mostly clear, lacks delivery (4–7 pts) | Concise, memorable, clear pitch (8–10 pts)
- c. Visual Representation (10 pts): Not present in pitch deck (0 pts) | Present in pitch deck (10 pts) — **binary, easy points**

**2. Problem-Solving (25 pts)**
- a. Problem Significance (5 pts): Vague/unimportant (0–2 pts) | Clearly defined but not widespread (3–4 pts) | Widespread, target audience clearly defined (5 pts)
- b. Solution Definition and Efficiency (10 pts): Barely addresses problem (0–3 pts) | Addresses but has inefficiencies (4–7 pts) | Directly and efficiently addresses (8–10 pts)
- c. Realism and Practicality (10 pts): Unrealistic/impractical technology (0–3 pts) | Mostly practical, some unrealism (4–7 pts) | Practical with reasonable limitations (8–10 pts)

**3. Target Market (12 pts)**
- a. Market Analysis (12 pts): Vague customers, competitors ignored (0–6 pts) | Customers clearly defined, aware of competition (7–12 pts)

**Qualifier Tie Breakers:** 1st — Higher presentation clarity score | 2nd — Higher problem-solving score | 3rd — Majority judge vote

### Finals Rubric (33 pts total)

**1. Solution Quality and Realism (12 pts):** Poor/unrealistic (0–3) | Realistic but not most efficient (4–8) | Realistic and most efficient (9–12)

**2. Depth/Defense of Reasoning (11 pts):** Shallow/vague, poorly defended (0–4) | Decent, not optimal (5–7) | Optimal, well-defended (8–11)

**3. Clarity and Presentation of Solution (10 pts):** Poorly presented (0–3) | Presented well, some parts unclear (4–6) | Clear and eloquent (7–10)

**Finals Tie Breakers:** 1st — Higher total finals score | 2nd — Higher Solution Quality score | 3rd — Higher Depth/Defense score | 4th — Higher Clarity score | Final — Majority judge vote

### Competition Rules
- Max 3 people per team
- No graphic or inappropriate products — disqualification
- Disrespect to other teams or judges — disqualification
- No products that are or represent a weapon
