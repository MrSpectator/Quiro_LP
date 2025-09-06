# Quiro Landing Page (Plain HTML/CSS/JS)

A lightweight, mobile-first landing page for Quiro (University Management Solution) built with:
- TailwindCSS (CDN)
- GSAP animations (CDN)
- Particles.js (CDN)
- Plain JavaScript (no build step)

This repo also includes a pricing page.

## Getting Started

1. Open `index.html` in a modern browser (Chrome, Edge, Firefox, Safari).
2. Optional: Serve locally for smoother testing (cache/headers):
   - Using Python: `python -m http.server 8000` then visit `http://localhost:8000`
   - Using VS Code Live Server or any static server

## Structure

- `index.html` — Main landing page
  - Hero with mist animation, particles, and animated "Coming Soon" badge
  - Features grid
  - Potential Impact counters
  - Modules Breakdown carousel (auto-play with ‹/› controls)
  - CTA form integrated with Formspree
  - Footer with WhatsApp contact
- `pricing.html` — Standalone Pricing Plans page
- `images/` — Assets directory
  - `about-hero.jpg` — Used for hero background and favicon

## Configuration

- Formspree endpoint: configured to `https://formspree.io/f/mzzaklgw` in both forms. Replace if needed in `index.html`.
- WhatsApp contact: `https://wa.me/2348120409164` in the footer.
- Favicon: points to `images/about-hero.jpg`. For a perfect circular favicon, replace with a circular PNG/JPG and update the link if desired.

## Customization

- Colors and font are configured inline via Tailwind CDN:
  - Colors: Black `#000000`, Emerald `#10B981`, Blue `#1E3A8A`
  - Font: Inter (Google Fonts)
- Hero background: update the `src` of the hero `<img>` in `index.html`.
- Coming Soon speed/behavior: tweak CSS keyframes `typingCycle` and `.coming-cycle` in `<style>`.
- Modules carousel: edit the `modules` array in the bottom `<script>` of `index.html`.

## Performance Tips

- Use compressed images (≤500KB each). Tools: TinyPNG, Squoosh.
- Host on a static CDN (Netlify/Vercel/Cloudflare Pages) for fast delivery.
- Because Tailwind is via CDN, no build step is required. For production hardening, you can prebuild a purged CSS, but it’s optional.

## Deployment

- Netlify/Vercel: Drag-and-drop the folder or connect the repo (static site).
- GitHub Pages: Push and enable Pages for the repository; set root to `/`.

## Pricing Page Content

`pricing.html` includes the following sections:
- SaaS (Per Module/Year): Core, Advanced, Specialized
- White-Label: Standard (<10,000 students), Enterprise (>10,000 students)
- Per-Student (Per Year): Small, Medium
- Training & Support: Basic, Premium
- SMS/Email Credits: Pay-as-you-go, Bundle
- Example, discount, and contract notes

## Accessibility

- Text contrast follows a high-contrast black/white theme with accented colors.
- Interactive controls (‹/›) are buttons with `aria-label`s; auto-play pauses on hover.

## License

Proprietary — All rights reserved by Quiro. Contact for usage permissions.
