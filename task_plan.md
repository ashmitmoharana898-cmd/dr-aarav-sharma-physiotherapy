# Task Plan: Premium Physiotherapist Personal Brand Website (Google Stitch)

## Phase 1: Tooling Verification & Linking
- [x] Verify Stitch MCP CLI tool connectivity with `STITCH_API_KEY`.
- [x] Validate json input/output pipeline using `.tmp/` payload files.

## Phase 2: Stitch Project Initialization
- [x] Create Stitch Project: "Dr. Aarav Sharma - Physiotherapy".
- [x] Record Stitch Project ID: `projects/17221965482039666635`.

## Phase 3: Design System Setup in Stitch
- [x] Define Design System tokens:
  - Color Palette: Forest Green (`#183D32`), Warm Ivory (`#F7F6F0`), Muted Sage (`#A8B9A1`), Warm Beige (`#D9D2C5`), Charcoal (`#292E29`), White (`#FFFFFF`).
  - Typography: `PLAYFAIR_DISPLAY` (Headlines), `MANROPE` (Body).
  - Shape: `ROUND_TWELVE`.
- [x] Call `create_design_system` in Stitch (Asset ID: `assets/16903405018994326335`).

## Phase 4 & 5: Screen Generation & Geographical Refinement (India Context)
- [x] Generated original desktop homepage.
- [x] Localized to South Delhi, New Delhi, India & Indian clinical accreditations (`BPT, MPT, MIAP, DCP`).
- [x] Retained all demo statistics (4.9★ rating, 500+ patients, 12+ years experience, 5,000+ patient recoveries, 98% satisfaction rate, 1-on-1 care ratio, and complete testimonial stories).

## Phase 6: Reference Hero Composition & Full GSAP Animation Suite
- [x] Rebuilt Hero layout matching provided reference image (oversized watermark "Sharma", doctor cutout with bottom fade mask, floating badge, 3D glass spine).

## Phase 7: Blank Fix, Parallax Background & Fluid Scrub Testimonials
- [x] Fixed blank service cards: Replaced blocking initial `opacity: 0` with guaranteed visible DOM cards (`opacity: 1`) and non-blocking `gsap.fromTo(..., { immediateRender: false })`.
- [x] Added architectural wellness clinic parallax background (`assets/clinic_bg.jpg`) moving at a slower speed (`yPercent: -25`).
- [x] Added biomechanical kinetic motion wave vector layer moving with counter-depth (`yPercent: 18`).
- [x] Implemented fluid scroll scrub for testimonials: cards smoothly glide horizontally across as the user scrolls down through the section.
- [x] Verified HTTP 200 and refreshed `http://localhost:3000`.
