# Majestic Park Inn — Project Context & Documentation

## 1. Project Overview

**Majestic Park Inn** is a warm editorial boutique hotel and residences digital web experience. The website balances the quiet authority of an architectural monograph with the warmth and intimacy of a private luxury residence. Built with bespoke editorial layouts, warm tactile color palettes, razor-thin hairlines, and asymmetric rhythms, it presents modern hospitality rooted in contemporary Indian craftsmanship and residential tranquility.

---

## 2. Property Information & Metadata

| Property Attribute | Detail |
| :--- | :--- |
| **Brand Name** | Majestic Park Inn |
| **Subtitle / Concept** | Boutique Hotel & Residences • Contemporary Sanctuary |
| **Physical Address** | Khahaan, Vapi Trade Centre, Via Char Rasta Rd, Phase 1, GIDC, Vapi, Gujarat 396195 |
| **Coordinates** | `Lat. 20.3708° N • Long. 72.9106° E` |
| **Reservations Email** | [reservations@majesticparkinn.com](mailto:reservations@majesticparkinn.com) |
| **Concierge Email** | [concierge@majesticparkinn.com](mailto:concierge@majesticparkinn.com) |
| **Telephone** | [+91 (0) 260 243 0000](tel:+912602430000) |
| **Map Location** | [Google Search & Maps Location](https://www.google.com/search?q=majestic+park+inn+vapi+address) |

---

## 3. Repository Structure

```
stitch_warm_editorial_boutique_hotel/
├── code.html          # Main responsive single-page editorial website
├── DESIGN.md          # Design system specification and design tokens
├── screen.png         # Reference full-page visual design render
├── context.md         # Full project context, documentation, and technical guide
└── cotext.md          # Project context reference alias
```

---

## 4. Technical Stack

- **Markup & Structure:** Semantic HTML5 (`<!DOCTYPE html>`, semantic landmarks: `<header>`, `<main>`, `<section>`, `<nav>`, `<footer>`)
- **Styling Engine:** Tailwind CSS loaded via CDN (`https://cdn.tailwindcss.com`) with an inline `tailwind.config` matching the custom tokens in `DESIGN.md`.
- **Typography:**
  - `EB Garamond`: Classical serif typeface used for display hero banners, editorial headlines, and monograph quotes.
  - `Manrope`: Modern geometric sans-serif used for body copy, micro-labels, uppercase caps, and interactive triggers.
- **Iconography:** Google Material Symbols Outlined (`opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200`).
- **Interactions & Client Scripting:** Vanilla JavaScript (ES6+):
  - Fullscreen photo lightbox with image viewer and captions.
  - Interactive date pickers and party size selectors in the booking engine.
  - Dynamic availability confirmation toast notification.
  - Off-canvas responsive mobile drawer navigation.
  - Modal keyboard shortcuts (`Escape` key dismiss).

---

## 5. Design System & Aesthetic Language

### Visual Identity
- **Atmosphere:** Residential warmth, sunlight filtering through linen, honest natural materials (walnut, cane joinery, carved travertine, lime wash).
- **Geometric Language:** Sharp (`0px` border-radius) for cards, buttons, dialogs, and image containers, honoring stone joinery and Indian modernist architecture.
- **Contrast & Depth:** Diffused warm ambient shadows (`rgba(85, 59, 46, 0.08)`), tonal layering over `#fdf9f0` canvas, and razor-thin hairlines (`rgba(85, 59, 46, 0.15)`).

### Core Color Palette
| Token | Hex Code | Role |
| :--- | :--- | :--- |
| `surface` / `background` | `#fdf9f0` | Foundation warm ivory substrate |
| `surface-container-lowest` | `#ffffff` | Clean elevated cards and active inputs |
| `surface-container-low` | `#f7f3ea` | Subtle card backdrops and booking modules |
| `surface-container` | `#f1eee5` | Stat cards and layered content blocks |
| `on-surface` | `#1c1c16` | High-contrast display typography |
| `secondary` | `#75584a` | Subdued secondary copy, editorial subtitles, footer |
| `primary` | `#9e4200` | Warm terracotta brand accent |
| `primary-container` | `#e87532` | Interactive CTA button background |
| `tertiary-fixed` | `#ffdea5` | Warm gold divider lines and accent badges |
| `outline-variant` | `#dec1b4` | Hairline dividers and subtle container borders |

### Typography Scale
| Role | Font Family | Size / Line Height | Tracking / Weight |
| :--- | :--- | :--- | :--- |
| **Display Hero** | EB Garamond | `72px` / `80px` (Desktop)<br>`40px` / `48px` (Mobile) | `-0.02em` / `400` |
| **Headline Large** | EB Garamond | `48px` / `56px` | `-0.015em` / `400` |
| **Headline Medium** | EB Garamond | `36px` / `44px` | Normal / `400` |
| **Headline Small** | EB Garamond | `24px` / `32px` | Normal / `500` |
| **Title Editorial** | EB Garamond | `20px` / `28px` | Normal / `400` |
| **Body Large** | Manrope | `18px` / `30px` | `-0.005em` / `400` |
| **Body Medium** | Manrope | `15px` / `24px` | Normal / `400` |
| **Body Small** | Manrope | `13px` / `20px` | Normal / `400` |
| **Label Caps** | Manrope | `11px` / `16px` | `0.12em` Uppercase / `600` |
| **Button Text** | Manrope | `13px` / `18px` | `0.06em` Uppercase / `600` |

---

## 6. Page Sections Breakdown (`code.html`)

1. **Global Header & Navigation (`#global-header`)**:
   - Pinned top navigation bar with dynamic backdrop blur (`backdrop-blur-xl`).
   - Brand mark: "Majestic Park Inn — Boutique Hotel & Residences".
   - Links: Rooms & Suites, Dining, Experiences, Our Story.
   - Primary Call to Action: "Check Availability" + user profile quick-action.
   - Mobile hamburger toggle button.

2. **Mobile Drawer Navigation (`#mobile-drawer`)**:
   - Slide-in side drawer from the right.
   - Brand header with close icon (`close`).
   - Extended links including Holistic Wellness and Concierge & Enquiries.
   - Bottom booking CTA and geographic locator indicator ("Vapi • Gujarat").

3. **Hero Section**:
   - Immersive full-screen imagery with ambient zoom duration (`duration-[12000ms]`).
   - Editorial headline: *"Stay somewhere that feels like home."*
   - Geographic coordinates (`Lat. 20.3708° N • Long. 72.9106° E`).
   - Dual actions: Direct booking jump and suites exploration anchor.

4. **Architectural Booking Bar (`#booking-engine`)**:
   - Modular 12-column grid container overlapping the hero boundary.
   - Fields: Check-in date picker, Check-out date picker, Party Size select, Suite Preference select.
   - Interactive search action with instant availability toast feedback (`#booking-toast`).

5. **Philosophy & Editorial Narrative**:
   - Asymmetric two-column composition (5 cols narrative, 7 cols visual showcase).
   - Core metrics: 28 Curated Suites, 02 Artisan Salons, 100% Quiet Living.
   - Decorative floating pull-quote box citing the Spatial Journal.

6. **Suites & Sanctuaries Showcase (`#suites`)**:
   - Alternating editorial layout featuring The Premier Studio Suite, Executive Living Suite, and Terrace Courtyard Suite.
   - Micro-amenity pill tags (King Linen Bedding, Concealed Cove Glow, Carved Travertine Bath, Specialty Bean Bar).

7. **Sensory Dining & The Verandah Restaurant**:
   - Inverted dark container (`#2E241F`) celebrating culinary architecture.
   - Monochrome Italian marble flooring, luminous hand-blown amber pendants, seasonal small-batch pairings.

8. **Visual Monograph & Lightbox Modal (`#gallery-lightbox`)**:
   - Curated photo gallery featuring bedroom sanctuaries, cane furniture details, and dining tables.
   - Interactive zoom view on click, managed via JavaScript `openLightbox()` and `closeLightbox()`.

9. **Heritage & Ethos (`#ethos`)**:
   - Deep dive into tactile materials: natural lime wash, solid Indian rosewood and walnut, raw cane webbing.
   - Resident Curations: Extended Creative Sabbatical, Architectural & Heritage Immersion, Slow Food & Wine Flight.

10. **Closing Call to Action**:
    - High-impact closing banner inviting direct bookings with guaranteed best rates, artisan breakfast, and flexible arrival.

11. **Editorial Footer**:
    - Complete property branding, address in Vapi, Gujarat, direct contact emails, telephone, and social/map links.
    - Newsletter subscription dispatch form.
    - Legal navigation (Privacy Policy, Terms of Stay, Accessibility).

---

## 7. Maintenance & Modification Guide

- **Updating Hotel Information:**
  - Brand name, coordinates, address, and phone numbers are declared in semantic tags in `code.html`.
  - Maintain synchronization between desktop header, mobile drawer, hero subtitles, and footer address blocks.
- **Adding / Modifying Suites:**
  - Follow the asymmetric column grid layout in the `#suites` section.
  - Use high-resolution photography with `4:3` or `16:10` aspect ratios and zero border radius.
- **Form Handling:**
  - The booking engine form (`#majestic-booking-form`) intercepts submit events and triggers the courtesy status toast. To integrate an external booking engine (e.g., SynXis, Cloudbeds, or customized booking API), update the event listener in `<script>`.
