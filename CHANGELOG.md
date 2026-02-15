# Changelog

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
