# Changelog

## 2026-02-16 — Landing Page Redesign

### Design
- Complete visual redesign: dark background (#0D0D0D) with vibrant gradient accents (magenta/coral/purple)
- New typography system: Space Grotesk (headings), Inter (body), JetBrains Mono (monospace accents)
- Oversized gradient text effect on name (white → magenta → coral)
- Animated gradient ring around profile photo (magenta → purple → coral, 8s rotation)
- Pulsing radial glow behind photo
- Staggered fade-in animations for hero, about, and links sections
- Card-style link buttons with lift-on-hover and magenta glow shadow
- Pill-shaped credential/skill badges with hover effects

### Content
- Updated role: "Senior Web Developer" → "Software Engineer at Atlassian"
- Added tagline: "Simple solutions to complex software problems."
- Added location: Auckland, New Zealand
- Added badges: AWS Certified Solutions Architect, Data Visualization, Viz for Social Good
- Replaced X/Twitter link with GitHub (github.com/maryzam)
- Updated LinkedIn URL to nz.linkedin.com/in/maryzam

### Structure
- New semantic HTML: header (hero) / main (about) / footer (links)
- Clean 24×24 stroke-style SVG icons (Feather-style) replacing filled circle icons
- Added aria-labels on link cards and aria-hidden on decorative elements
- Added focus-visible styles for keyboard navigation

### Responsive & Accessibility
- Mobile breakpoint at 640px: stacked hero, centered badges, full-width link cards
- Fluid typography with clamp() for hero name
- `prefers-reduced-motion` media query disables all animations
- Font preconnect hints for faster loading

## 2026-02-16 — Technical Modernization & Bug Fixes

### Bug Fixes
- Fixed CSS syntax error — `width: 50%:;` corrected to `width: 50%;` in `styles.css`
- Removed `overflow: hidden` from `*` selector — was breaking scrolling and clipping content globally
- Removed empty `scripts/main.js` and its `<script>` tag — dead code

### Technical Modernization
- Added `<meta name="viewport">` — the site now renders correctly on mobile devices
- Added `lang="en"` to `<html>` tag — accessibility and SEO
- Added SEO meta tags — `description`, Open Graph (`og:title`, `og:description`, `og:image`, `og:type`) for proper link previews
- Added emoji favicon — no more blank browser tab icon
- Upgraded Google Fonts URL to `css2` API with `display=swap` — prevents render-blocking font load
- Added `loading="lazy"` to the profile image
- Replaced all hardcoded colors with CSS custom properties — `--color-text`, `--color-bg`, `--color-gradient-1`, etc. in `:root`
- Added responsive media query (`max-width: 600px`) — stacks layout vertically on mobile, scales avatar to 40%
- Updated Twitter to X — new URL (`x.com`), new SVG icon, updated title attribute
