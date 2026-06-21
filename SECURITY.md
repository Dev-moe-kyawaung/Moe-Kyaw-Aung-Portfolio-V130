# 🔒 Security Policy — Moe Kyaw Aung Portfolio V130

## Supported Versions

| Version | Status | Support |
|---------|--------|---------|
| V130 (latest) | ✅ Active | Full support |
| V123 | ⚠️ Legacy | Critical fixes only |
| V86 and below | ❌ EOL | No support |

---

## 📧 Reporting a Vulnerability

Please use **responsible disclosure** — do not create public GitHub issues for security vulnerabilities.

### Contact

| Method | Details |
|--------|---------|
| 📧 **Email** | moekyawaung@gmail.com |
| 💬 **Telegram** | [@moekyawaung](https://t.me/moekyawaung) |
| **Subject line** | `[SECURITY] V130 – Brief description` |

### What to Include

1. Vulnerability type and severity (Critical / High / Medium / Low)
2. Affected file and line number (if known)
3. Step-by-step reproduction instructions
4. Proof-of-concept (screenshots, code snippet)
5. Potential impact assessment
6. Suggested remediation (optional)

---

## ⏱️ Response Timeline

| Stage | Timeline |
|-------|----------|
| Acknowledgement | Within 48 hours |
| Initial assessment | Within 5 business days |
| Fix for Critical/High | Within 7 days |
| Fix for Medium/Low | Within 30 days |
| Public disclosure | After fix deployed + 7 days |

---

## 🎯 Scope

### In Scope ✅
- Cross-site scripting (XSS) via user-input fields (contact form, newsletter)
- Content injection through URL parameters
- PWA Service Worker hijacking vulnerabilities
- Privacy data exposure in client-side code
- Open redirect vulnerabilities
- Insecure external resource loading (CDN integrity)

### Out of Scope ❌
- Self-XSS (requires victim to execute code themselves)
- Theoretical / no-impact vulnerabilities
- Bugs in Bootstrap, Font Awesome, or other third-party CDN libraries
  (please report those directly to their maintainers)
- Social engineering / phishing attacks
- Issues only affecting unsupported browser versions (IE 11, etc.)
- Rate limiting on the static GitHub Pages host

---

## 🛡️ Security Design Decisions

| Decision | Rationale |
|----------|-----------|
| All external links use `rel="noopener noreferrer"` | Prevents tab-napping / reverse tabnapping |
| No API keys or secrets in source code | Static portfolio — all data is public |
| Form validation (client-side) | UX feedback; server-side validation not applicable (static site) |
| CDN resources loaded via HTTPS | Prevents mixed-content attacks |
| No `eval()` or `new Function()` | Eliminates code injection via these vectors |
| Blob URL for PWA manifest | Avoids manifest path enumeration |
| `Content-Security-Policy` compatible | No unsafe-inline JS (all JS is in `<script>` blocks, not attributes) |

---

## 🏆 Hall of Fame

Researchers who responsibly disclosed vulnerabilities will be credited here.

| Researcher | Vulnerability | Date | Severity |
|-----------|--------------|------|---------|
| *(None yet)* | — | — | — |

---

## 📜 Commitment

- We will **not pursue legal action** against researchers following this policy
- We will **credit** responsible disclosers in CHANGELOG and Hall of Fame (if desired)
- We will **communicate transparently** about the fix timeline
- We will **not silence** valid security reports

---

*Thank you for helping keep this project secure. 🙏*  
*— Moe Kyaw Aung · [github.com/Dev-moe-kyawaung](https://github.com/Dev-moe-kyawaung)*
