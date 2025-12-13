## 2025-05-20 - Improved Button Accessibility and Navigation
**Learning:** Using `next/link` instead of `window.location.href` on buttons not only improves SPA performance but also allows for proper semantic HTML (links vs buttons). Decorative SVGs should always have `aria-hidden='true'` to avoid confusing screen readers.
**Action:** Always check for interactive elements using incorrect semantics (button vs link) and ensure decorative icons are hidden from AT.
