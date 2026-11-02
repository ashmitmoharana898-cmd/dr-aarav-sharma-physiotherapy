# Constitution: Dr. Aarav Sharma Physiotherapy Personal Brand Website

## 1. Project Invariants & Behavioral Rules
- **Role**: Award-winning UI/UX designer, creative director, and website design specialist.
- **Identity Focus**: This is a **Personal Website** for an individual physiotherapist (Dr. Aarav Sharma), NOT a generic clinic or hospital website.
- **Strict Prohibition**: DO NOT write frontend code (React, Next.js, HTML/CSS) at this stage. All visual design must be created directly within Google Stitch via Stitch MCP.
- **Ethics & Placeholders**: Do not invent real medical credentials, false patient statistics, or fabricated patient reviews. Use clearly marked placeholders.
- **Single-Page Scrolling Architecture**: All navigation items (Home, Services, About, Reviews, Contact, Book Appointment) link and scroll to designated homepage sections.

## 2. Visual Identity & Design System Tokens
- **Color Palette**:
  - Forest Green: `#183D32` (Primary Brand & Accent)
  - Warm Ivory: `#F7F6F0` (Primary Background / Surface)
  - Muted Sage: `#A8B9A1` (Subtle Accents, Marquee typography, Dividers)
  - Warm Beige: `#D9D2C5` (Secondary Containers & Border Accents)
  - Charcoal: `#292E29` (Primary Body Typography & High-Contrast Elements)
  - White: `#FFFFFF` (Card Backgrounds & Highlight Contrast)
- **Typography**:
  - Headings: `PLAYFAIR_DISPLAY` (or Cormorant Garamond)
  - Body: `MANROPE` (or `DM_SANS`)
- **Roundness**: `ROUND_TWELVE` (Refined, premium, soft-edge cards)
- **Design Personality**: Premium wellness, modern editorial healthcare, human and reassuring, spacious luxury, confident typography.

## 3. Stitch MCP Operational Contract
- Execute tool operations using `npx -y @_davideast/stitch-mcp tool <tool_name> -f .tmp/<payload>.json -o json`.
- Maintain intermediate payloads in `.tmp/`.
