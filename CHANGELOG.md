# 📋 Changelog — Moe Kyaw Aung Portfolio

All notable changes documented following [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) format.

---

## [V130] — 2026-06-07 🚀 **CURRENT RELEASE**

### ✨ Added — New Sections
- 10-page multi-section SaaS/Landing portfolio (4,500+ lines, single HTML)
- Interactive particle canvas hero (140 particles + WebGL-style connection lines)
- SVG animated skill rings ×8 (Kotlin 96% / Compose 90% / Firebase 88% / MVVM 93% / CI-CD 85% / Room 91% / REST 94% / Testing 82%)
- Playable Snake Game easter egg (Canvas API, WASD + arrow keys, score tracker)
- Multi-language toggle (English · မြန်မာ · 中文 · 日本語 · 한국어 · ภาษาไทย)
- Full မြန်မာဘာသာ (Burmese language) dedicated section
- PWA Service Worker with cache-first offline strategy
- Dynamic Web App Manifest (inline blob URL — no extra file needed)
- PWA install banner with `beforeinstallprompt` event handler
- JSON-LD Schema.org structured data (`Person` + `WebSite` types)
- Technology comparison table (16 techs with version/proficiency/production matrix)
- GitHub contribution heatmap (52 weeks × 7 days, hover tooltips)
- Repo stats horizontal bar chart (top 6 repos by commits)
- Full animated tech skill cloud (54 technology tags with float animation)
- Blog & Articles section (6 technical Android posts with thumbnails)
- Video showcase section (background video + dual CTA buttons)
- Share modal (LinkedIn / Twitter/X / Telegram / Copy link)
- Read progress indicator bar (top fixed bar, 0–100% on scroll)
- Neon cursor trail (10-dot fading animation following mouse)
- Floating hero tech badge labels (10 tags orbiting hero)
- Keyboard shortcuts: H=Hero / C=Contact / G=GitHub / /=CertSearch / Esc=Close lightbox
- Click-to-copy on all email addresses (Clipboard API + toast feedback)
- Open Source activity section (heatmap + repo stats + contribution summary)
- Achievements & Awards section (7 milestone cards with years)
- Multi-locale Open Graph (`og:locale:alternate` EN + MM)
- Custom scrollbar styles (WebKit + Firefox scrollbar-color)
- Print stylesheet (hides cursor, nav, CTAs for clean print output)
- Footer "Share Portfolio" and theme toggle buttons
- 43 GitHub account cards (dynamic JS render — no duplication)
- 18+ Lovable PWA links (dynamic JS render)
- 82+ certificate cards (live search + 9-category filter)
- 8 organization/community affiliation cards
- 9 feature highlight cards (Clean Arch / Compose / Firebase / CI-CD / Security / Offline / Testing / Multi-module / API)
- 16+ app cards in Masonry/Pinterest grid layout
- 6-address email collection section (click-to-copy)
- 4-client testimonial carousel (auto-rotate 5.5s, dot nav, prev/next arrows)
- 3-tier pricing table ($2.5K Starter / $5.5K Pro / $9K Enterprise)
- 7-question FAQ accordion with smooth max-height animation
- 8-image photo gallery with ESC-closeable lightbox
- Google Maps embed (Yangon, Myanmar — dark filter)
- Newsletter subscription form with regex validation
- Contact form (5 fields + select + textarea + full validation)
- Animated statistics counter (12+ yrs / 3K+ apps / 122 repos / 100%)
- Parallax scrolling on section background layers
- Scroll-triggered fade-in / fade-left / fade-right animations
- Stagger animation delays (.stagger-1 through .stagger-5)
- IntersectionObserver for all scroll animations + image lazy loading
- 30 animated progress bars (6 categories × 5 bars)

### 🎨 Design System
- Cyberpunk / Neon aesthetic direction
- Electric Orange (#e8590c) CSS custom property system
- Dark backgrounds: #0d0d0d / #111111 / #1a1a1a / #222222
- Warm white (#FFF7ED) text palette
- Accent colors: Cyan (#00f5ff) · Purple (#b347ea) · Green (#39ff14) · Yellow (#ffd700)
- Orbitron (headings) + Rajdhani (body) + Share Tech Mono (code) + Noto Sans Myanmar
- Full dark ↔ light mode via CSS `[data-theme]` attribute
- 30+ CSS custom properties (design tokens)
- Custom neon cursor (dot + expanding ring on hover)
- Neon dividers between all sections (pulsing glow animation)

### ⚡ Performance
- Single HTML file — zero npm dependencies, zero build step
- All images via Cloudinary CDN (auto WebP, lazy-loaded)
- Canvas particle animation (requestAnimationFrame, 60fps target)
- Bootstrap 5.3.3 + Font Awesome 6.5.0 via JSDelivr/Cloudflare CDN
- Gzip estimate: ~65KB (72% compression from 236KB raw)
- IntersectionObserver for lazy image loading (200px rootMargin)

### 🔒 Security
- All external links: `rel="noopener noreferrer"`
- No `eval()` or dynamic code injection
- Form validation: client-side (name/email/message length)
- No sensitive keys or tokens in source code
- PWA manifest served as `blob:` URL (no manifest file path exposure)
- CSP-friendly (no inline event handlers on critical elements)

---

## [V123] — 2026-05-20

### Added
- Flutter/Dart cyberpunk theme variant
- Teal/cyan alternate color scheme
- Multi-module architecture showcase
- CI/CD pipeline visualization diagram

### Changed
- Upgraded from V86 base structure
- Refactored all CSS to custom property system
- Added deep Jetpack Compose section

---

## [V86] — 2026-05-01

### Added
- Glasspunk theme (soft purple/lavender)
- Light mode as default theme
- Certificate gallery (60+ certs)
- GitHub accounts section (first version, 30 accounts)
- Gravatar profile embed

### Changed
- Migrated from multi-file to single HTML
- CSS consolidated into `<style>` block
- Font changed to Poppins + Fira Code

---

## [V64] — 2026-04-10

### Added
- Electric Orange cyberpunk theme (early V130 ancestor)
- Particle hero (basic version, 80 particles)
- First animated skill bars
- Testimonial section

### Changed
- Grid layout improved to CSS Grid
- Mobile hamburger menu added

---

## [V50] — 2026-03-15

### Milestones
- First PWA support (basic manifest + service worker)
- Service worker offline fallback page added
- First dark/light toggle (simple class-based)

---

## [V30] — 2026-02-01

### Foundation
- GitHub Pages deployment configured
- First certificate gallery (40 certs)
- LinkedIn + GitHub social icons
- Basic responsive grid (Bootstrap 4)

---

## [V10] — 2026-01-05

### Foundation
- Bootstrap 5 framework adopted
- Mobile-first responsive layout
- Hero section with static avatar
- About + Skills sections

---

## [V1] — 2025-12-01

### Initial Release
- First HTML/CSS personal portfolio
- 3 sections: Hero · About · Contact
- Basic Google Fonts integration
- Deploy to GitHub Pages

---

*Maintained by [Moe Kyaw Aung](https://github.com/Dev-moe-kyawaung) · Myanmar 🇲🇲 · 2026*
