# 🤝 Contributing to Moe Kyaw Aung Portfolio V130

Thank you for your interest in contributing! 🎉  
This is a personal portfolio project — contributions are welcome for bug fixes, accessibility improvements, and performance enhancements.

---

## 🚦 Before You Start

1. **Search existing issues** — your bug or idea may already be tracked
2. **Open an issue first** for major changes (discuss the approach before coding)
3. **Keep PRs focused** — one topic per pull request

---

## 🔧 Local Development Setup

```bash
# 1. Fork this repository on GitHub (click Fork button)

# 2. Clone your fork
git clone https://github.com/YOUR-USERNAME/Moe-Kyaw-Aung-Portfolio-V130.git
cd Moe-Kyaw-Aung-Portfolio-V130

# 3. Create a feature/fix branch
git checkout -b fix/testimonial-carousel-timing
# or
git checkout -b feat/japanese-language-section
# or
git checkout -b docs/update-github-accounts-list

# 4. Start a local server (required for PWA features)
python3 -m http.server 8080
# Open: http://localhost:8080

# 5. Make changes in index.html
# (All code is in one file — no build step)

# 6. Test thoroughly (see Testing Checklist below)

# 7. Commit with Conventional Commits format
git add .
git commit -m "fix: correct testimonial carousel dot indicator sync"

# 8. Push and open a Pull Request
git push origin fix/testimonial-carousel-timing
```

---

## 📋 Pull Request Checklist

Before submitting your PR, ensure:

```
Browser Testing
  [ ] Chrome (latest stable)
  [ ] Firefox (latest stable)
  [ ] Safari (latest, macOS or iOS)
  [ ] Edge (latest stable)
  [ ] Mobile Chrome (Android)
  [ ] Mobile Safari (iOS)

Responsive Testing
  [ ] 320px  — small mobile (Samsung Galaxy S5, iPhone SE)
  [ ] 375px  — standard mobile (iPhone 12/13/14)
  [ ] 414px  — large mobile (iPhone Pro Max)
  [ ] 768px  — tablet portrait (iPad)
  [ ] 1024px — tablet landscape / small laptop
  [ ] 1280px — laptop
  [ ] 1440px — desktop
  [ ] 1920px — full HD

Feature Testing
  [ ] Dark mode works correctly with change
  [ ] Light mode works correctly with change
  [ ] Scroll animations trigger correctly
  [ ] No console errors (DevTools → Console)
  [ ] No broken images (DevTools → Network)
  [ ] PWA install still works
  [ ] Snake game still functional
  [ ] Certificate search/filter functional
  [ ] Contact form validation works
  [ ] All 43 GitHub cards render
  [ ] All 18+ Lovable cards render

Code Quality
  [ ] Comments added for complex logic
  [ ] CSS uses custom properties (no hardcoded colors)
  [ ] External links have rel="noopener noreferrer"
  [ ] Images have descriptive alt text
  [ ] CHANGELOG.md updated under [Unreleased]
  [ ] README.md updated if new features added
```

---

## 📝 Commit Message Convention

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```bash
# Format:
<type>(<scope>): <short description>

# Types:
feat     # New feature or section
fix      # Bug fix
docs     # Documentation only
style    # CSS/visual changes (no logic change)
perf     # Performance improvement
a11y     # Accessibility improvement
refactor # Code restructuring (no feature/fix)
test     # Adding or fixing tests
chore    # Build, CI, config changes
security # Security improvement

# Examples:
feat(multilang): add Korean language support
fix(carousel): prevent dot indicator desync on rapid click
docs(readme): update Lovable PWA links table
style(hero): increase avatar border width to 4px
perf(canvas): reduce particle count on mobile to 60
a11y(nav): add aria-label to social icon links
security(form): add honeypot field to contact form
```

---

## 🎨 Code Style Guide

### HTML
```html
<!-- ✅ Use semantic elements -->
<section id="skills" class="section-wrap" aria-label="Skills section">
  <div class="container">
    <!-- Comment major logical blocks -->
  </div>
</section>

<!-- ✅ Attribute order: id → class → type → href/src → data-* → aria-* -->
<button id="themeBtn" class="btn-theme" type="button" aria-label="Toggle theme">

<!-- ✅ External links always have rel attribute -->
<a href="https://github.com" target="_blank" rel="noopener noreferrer">GitHub</a>

<!-- ❌ Avoid: inline styles -->
<div style="color: #e8590c">  ← use CSS class instead
```

### CSS
```css
/* ✅ Always use CSS custom properties for colors */
color: var(--primary);           /* ✅ */
color: #e8590c;                  /* ❌ hardcoded */

/* ✅ Group properties logically */
.card-neon {
  /* 1. Layout */
  display: flex;
  flex-direction: column;
  gap: 1rem;

  /* 2. Box model */
  padding: 1.75rem;
  border-radius: var(--radius-lg);

  /* 3. Visual */
  background: var(--surface);
  border: 1px solid var(--border2);

  /* 4. Typography */
  font-family: var(--font-body);

  /* 5. Animation */
  transition: var(--transition);
}

/* ✅ Responsive: mobile-first */
.stats-grid {
  grid-template-columns: 1fr;         /* mobile default */
}
@media (min-width: 768px) {
  .stats-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (min-width: 1024px) {
  .stats-grid { grid-template-columns: repeat(4, 1fr); }
}
```

### JavaScript
```javascript
// ✅ Use const/let — never var
const PARTICLE_COUNT = 140;
let currentTestimonialIndex = 0;

// ✅ Arrow functions for callbacks
particles.forEach(p => p.update());

// ✅ Comment non-obvious logic
// Threshold 0.12 = trigger when 12% of element is visible
// Lower value = earlier trigger (good for tall sections)
const observer = new IntersectionObserver(callback, { threshold: 0.12 });

// ✅ Guard against null DOM elements
const certSearch = document.getElementById('certSearch');
if (certSearch) {
  certSearch.addEventListener('input', filterCerts);
}

// ✅ Descriptive function names
function animateSkillRingsOnScroll(entries) { /* ... */ }
function toggleFAQItem(clickedButton) { /* ... */ }
function showToastNotification(message, durationMs = 3500) { /* ... */ }

// ❌ Avoid: ambiguous names
function doStuff(e) { }     // unclear
function h(el) { }          // too short
```

---

## 🐛 Bug Report Template

Use [GitHub Issues](https://github.com/Dev-moe-kyawaung/Moe-Kyaw-Aung-Portfolio-V130/issues/new?template=bug_report.md):

**Required info:**
- Browser name and version
- Operating system + device type
- Screen width at time of bug
- Steps to reproduce (numbered list)
- Expected vs actual behavior
- Screenshot or screen recording
- Console errors (F12 → Console)

---

## 💡 Feature Request Guidelines

**Accepted contributions:**
- ✅ Accessibility improvements (ARIA, keyboard nav, color contrast)
- ✅ Mobile UX improvements (touch targets, swipe gestures)
- ✅ Performance optimizations (reduce repaints, lazy loading)
- ✅ Additional language translations
- ✅ New interactive features that fit the cyberpunk aesthetic
- ✅ Bug fixes and browser compatibility fixes

**Not currently accepted:**
- ❌ Changing the core Electric Orange color scheme (open an issue to discuss)
- ❌ Adding npm/build tool dependencies (must stay zero-dependency)
- ❌ Removing existing sections
- ❌ Replacing Bootstrap with another framework

---

## 🏆 Contributor Recognition

Contributors are recognized in:
- `CHANGELOG.md` under the relevant version
- A future Contributors section in `README.md`

---

*Thank you for contributing! Every improvement helps.* ⭐  
*— Moe Kyaw Aung · [github.com/Dev-moe-kyawaung](https://github.com/Dev-moe-kyawaung)*
