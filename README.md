# Dr. Aarav Sharma — Consultant Physiotherapist Personal Brand Website

> **Award-winning, editorial healthcare digital experience for Dr. Aarav Sharma (BPT, MPT, MIAP, DCP Reg.), Consultant Musculoskeletal & Sports Physiotherapist based in Greater Kailash II (GK-2), South Delhi, India.**

[![Live Demo](https://img.shields.io/badge/Demo-Live%20Online-183D32?style=for-the-badge&logo=google-chrome&logoColor=white)](https://ashmitmoharana898-cmd.github.io/dr-aarav-sharma-physiotherapy/)
[![Architecture](https://img.shields.io/badge/Architecture-Single--Page%20Parallax%20%2B%20Zero--Dep%20Backend-A8B9A1?style=for-the-badge)](https://github.com/ashmitmoharana898-cmd/dr-aarav-sharma-physiotherapy)
[![License](https://img.shields.io/badge/License-MIT-D9D2C5?style=for-the-badge)](LICENSE)

---

## 🌿 Overview & Creative Direction

Designed specifically as an **individual physiotherapist personal brand** (rather than a generic clinic), this platform blends clinical authority with the warmth and tranquility of a luxury South Delhi wellness sanctuary.

### Design Tokens & Visual Identity
- **Forest Green** (`#183D32`): Clinical authority, grounding, reassurance
- **Warm Ivory** (`#F7F6F0`): Clean, serene primary canvas
- **Muted Sage** (`#A8B9A1`): Calming kinetic accents & sub-elements
- **Travertine Beige** (`#D9D2C5`): Tactile border styling & structural containers
- **Charcoal** (`#292E29`): High-contrast editorial typography
- **Typography**: Editorial serif headings (`Playfair Display`) paired with precision geometric body copy (`Manrope`)

---

## ✨ Key Features & Motion Engineering

1. **Editorial Hero Section**:
   - Oversized *"Sharma"* watermark background typography with subtle parallax depth.
   - High-resolution doctor portrait with smooth bottom gradient fade mask.
   - Floating 4.9★ trust badge and 5,000+ patient social proof stack.
   - **Interactive 3D Translucent Glass Spine Sculpture** with levitation physics and responsive cursor parallax tilt (`rotationX` / `rotationY`).

2. **Full-Width Photographic Parallax Banner (`#cinematic-parallax`)**:
   - Oversized 120% photographic background (`assets/treatment_session.jpg`).
   - True 1:1 scroll-linked vertical translation: moves upward by ~22% as the user scrolls down, and downward when scrolling up.
   - 45% semi-transparent dark overlay for razor-sharp readability of editorial quotes and clinical trust metrics.

3. **Specialised Clinical Services with Quick-Filter Bar**:
   - 6 specialized care cards (Spine & Neck, Sports Rehab, Joint Care, Post-Op, Neurological, Ergonomics).
   - Dynamic symptom filter bar for instant condition matching.
   - Interactive **Clinical Treatment Protocol Modal** detailing techniques, timelines, and session structures.

4. **Pinned Horizontal Testimonial Carousel**:
   - Horizontal scroll scrub driven by natural mousewheel vertical scrolling on desktop with real-time dot indicators.

5. **Concierge Consultation Booking Sanctuary**:
   - Interactive In-Clinic (GK-2, South Delhi) vs. Virtual consultation toggle with reactive guidance.
   - HTML5 date picker (auto-initialized with minimum date of today and default tomorrow) alongside 3 daily consultation windows.
   - **Booking Confirmation Modal** generating reference ID `#AS-GK2-XXXX`.
   - **Dynamic `.ics` Calendar File Generation**: One-click download of calendar invitation matching the patient's exact chosen date and timeslot.

6. **Floating Concierge Controls**:
   - Direct 1-tap **WhatsApp Desk Widget** linking to `+91 98110 24891`.
   - Animated **Back-to-Top Button** fading in after 400px of scroll.

---

## 🛡️ Bulletproof Backend Architecture & Error Handling Patterns

Built using **pure Node.js standard libraries** (`http`, `fs`, `path`, `crypto`, `url`) with **zero external dependencies**:

- **Fail-Fast Input Validation**: Strict validation and HTML sanitization for patient name, phone, email, condition, mode, date, timeslot, and DPDP consent.
- **Domain-Specific Error Hierarchy**: Structured classes (`AppError`, `ValidationError`, `RateLimitError`, `NotFoundError`) returning standardized client response envelopes.
- **Atomic File Persistence**: Patient requests are written to temporary staging files (`data/.tmp-*.json`) before atomic renaming to `data/appointments.json`, preventing data loss or corruption during abrupt crashes.
- **Sliding-Window IP Rate Limiter**: Built-in in-memory rate limiting preventing form abuse or denial-of-service.
- **Graceful Degradation for Static Hosting**: When hosted statically (e.g., GitHub Pages) where `/api/book` returns 404, the frontend catches the network state gracefully, falls back to encrypted `localStorage`, and provides immediate confirmation without error dialogs.
- **Health Check Endpoint**: Real-time diagnostic monitoring available at `GET /api/health`.

---

## 🚀 Running Locally

### Prerequisites
- Node.js (v16 or higher)

### Quick Start
```bash
# Clone the repository
git clone https://github.com/ashmitmoharana898-cmd/dr-aarav-sharma-physiotherapy.git

# Navigate into the project
cd dr-aarav-sharma-physiotherapy

# Start the bulletproof server (zero npm install required!)
node server.js
```

Open your browser at **`http://localhost:3000`**.

### Available Endpoints
- `GET /` — Serves the full single-page application
- `GET /api/health` — Returns server uptime, memory, and status
- `POST /api/book` — Receives and atomically stores patient consultation bookings
- `GET /api/appointments` — Lists stored consultation bookings

---

## 📍 Clinic Location & Contact

- **Practice**: The Movement Sanctuary, Suite 402, Block E, Greater Kailash II (GK-2), South Delhi, New Delhi 110048, India
- **Desk**: `+91 98110 24891` / `+91 11 4165 0831`
- **Email**: `care@draaravsharma.in`

---

*© 2025 Dr. Aarav Sharma Physiotherapy. Member of Indian Association of Physiotherapists (MIAP) • Delhi Council for Physiotherapy & Occupational Therapy (DCP).*
