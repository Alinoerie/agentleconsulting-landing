# AgentleConsulting.com — Full Overhaul Plan
**Compiled by:** Orcha (COO)
**Date:** 2026-05-17
**Research sources:** Researcher + Dev + Marketing subagents

---

## RESEARCH SYNTHESIS

### Color Palette — Recommended Direction
Current site: Gold `#C49A3A` + Cream `#FAF8F5` + Dark `#111115` — good premium foundation

**Research consensus:** B2B AI consulting sites that convert best use:
- **Primary:** Deep indigo/slate (`#4338CA` range) — AI credibility without corporate blue fatigue
- **CTA accent:** Warm amber/orange (`#F59E0B`) — outperforms blue/green CTAs by up to 34%
- **Backgrounds:** Off-white (`#FAFAF9`) or warm cream — not pure white
- **Text:** Near-black (`#1E293B`) with warm undertone — never pure black on light

**Anti-patterns to avoid:**
- Pure white (`#FFFFFF`) — clinical, not premium
- Bright blue as dominant color — overused in SaaS
- Neon gold (`#FFD700`) — reads as "sale", not luxury
- Cool grey on cool white — creates flat, undifferentiated SaaS look

**Recommended new palette:**
```
--color-primary:    #3730A3  /* Deep indigo — authority, intelligence */
--color-primary-light: #4F46E5 /* Indigo hover */
--color-accent:     #F59E0B  /* Warm amber — CTA, urgency, human warmth */
--color-accent-hover: #D97706 /* Amber hover */
--color-bg:         #FAFAF9  /* Warm off-white — content background */
--color-bg-dark:    #0F172A  /* Near-black — hero, dark sections */
--color-surface:    #FFFFFF  /* Cards, elevated surfaces */
--color-text:       #1E293B  /* Near-black, warm — body text */
--color-text-muted: #64748B  /* Slate — secondary text */
--color-border:     #E2E8F0  /* Light border */
--color-gold:       #C49A3A  /* Keep existing gold — used sparingly */
```

### CTA Best Practices (from Dev research)
- **Button color:** Orange/warm amber outperforms blue/green by up to 34%
- **Copy:** First-person ("Book **My** Free Call") → up to 90% more clicks vs third-person
- **Placement:** Primary CTA above fold. ONE primary CTA per page — remove competing CTAs
- **Hero issue:** Currently has TWO CTAs ("Book..." AND "See How It Works") — splits focus

### Competitor USPs (from Marketing research)
Top AI automation consultants use:
1. Specific workflow focus (not "we automate everything")
2.透明 pricing with clear scope
3. Fast time-to-value ("live in 6 weeks")
4. Ownership/handover focus (you own the system)
5. Human access (direct to founder, not junior team)

### Technical Debt Summary (from Dev audit)
**HIGH priority (credibility + legal):**
1. GDPR cookie consent — needs proper opt-in architecture
2. Exit-intent popup — accessibility + aggression issue
3. European Accessibility Act — statement page required (deadline was June 2025)

**MEDIUM priority (performance + SEO):**
4. Images lack explicit width/height — hurts LCP + CLS
5. No LCP image preload
6. No image optimization (WebP conversion)

**LOWER priority:**
7. Two CTAs in hero — splits conversion focus
8. No hreflang tags for NL/BE/DE/UK targeting
9. OG tags — needs verification

---

## PHASED IMPLEMENTATION PLAN

### PHASE 1 — Visual Foundation (Design System)
**Owner:** Dev | **Goal:** New palette, typography, CSS variables, responsive polish

- [ ] 1.1 Update CSS variables with new color palette (indigo/slate + warm amber)
- [ ] 1.2 Update button styles: warm amber CTA buttons with dark text
- [ ] 1.3 Update link styles, form focus states to match palette
- [ ] 1.4 Typography audit — verify Playfair Display + Inter still appropriate
- [ ] 1.5 Verify font loading (preconnect, display=swap)
- [ ] 1.6 Hamburger menu: ensure full-screen overlay on mobile, proper z-index
- [ ] 1.7 Final mobile width fix — confirm no horizontal overflow anywhere

### PHASE 2 — Hero & CTA Optimization
**Owner:** Dev | **Goal:** Single focused CTA, above-fold conversion最大化

- [ ] 2.1 Consolidate hero to ONE primary CTA — remove "See How It Works" from hero
- [ ] 2.2 Change CTA copy to first-person: "Book My Free Discovery Call"
- [ ] 2.3 Verify CTA button is the single most visually dominant element on page
- [ ] 2.4 Move "See How It Works" to secondary position (below fold or nav)
- [ ] 2.5 Add fetchpriority="high" to hero background/image
- [ ] 2.6 Add explicit width/height to hero image

### PHASE 3 — Performance Fundamentals
**Owner:** Dev | **Goal:** Core Web Vitals green, LCP < 2.5s

- [ ] 3.1 Add `<link rel="preload">` for LCP image
- [ ] 3.2 Add explicit width/height to ALL images
- [ ] 3.3 Convert any remaining PNGs to WebP
- [ ] 3.4 Add loading="lazy" to below-fold images
- [ ] 3.5 Add preconnect hints for Google Fonts and Calendly
- [ ] 3.6 Verify OG meta tags (og:title, og:description, og:image, og:url)
- [ ] 3.7 Add Twitter Card meta

### PHASE 4 — Accessibility & Legal Compliance
**Owner:** Dev | **Goal:** WCAG 2.1 AA, European Accessibility Act compliance

- [ ] 4.1 Add alt text to all images (descriptive, not placeholder)
- [ ] 4.2 Verify all form fields have associated `<label>` elements
- [ ] 4.3 Add keyboard navigation test — ensure all interactive elements reachable
- [ ] 4.4 Verify focus states visible on all interactive elements
- [ ] 4.5 Fix exit-intent popup: keyboard dismissal (Esc), focus trap
- [ ] 4.6 Add `/accessibility.html` page — meets WCAG 2.1 AA standards
- [ ] 4.7 Audit cookie consent: proper opt-in (not just Accept/Reject)
- [ ] 4.8 Add skip-to-content link

### PHASE 5 — SEO & Structured Data
**Owner:** Dev | **Goal:** Full schema markup, hreflang, local SEO

- [ ] 5.1 Verify JSON-LD schema (Organization, ProfessionalService, FAQPage)
- [ ] 5.2 Add LocalBusiness schema with NL address
- [ ] 5.3 Add hreflang for en-EU, nl-NL, de-DE
- [ ] 5.4 Verify sitemap.xml — all pages, correct priorities
- [ ] 5.5 Add robots.txt if missing

### PHASE 6 — Content & Messaging
**Owner:** Marketing | **Goal:** Messaging aligns with research best practices

- [ ] 6.1 Update all CTA copy to first-person ("Book My..." not "Book a...")
- [ ] 6.2 Strip hype language (no "revolutionize", "best-in-class", "harness AI")
- [ ] 6.3 Add specific workflow names to services (not vague "automation")
- [ ] 6.4 Verify FAQ page — add qualifying questions (from Marketing research)
- [ ] 6.5 Review and update meta descriptions on all pages
- [ ] 6.6 Trust signals audit — remove anything that doesn't add credibility

### PHASE 7 — Trust & Social Proof
**Owner:** Marketing + Dev | **Goal:** Remove credibility gaps

- [ ] 7.1 Replace generated logos with real client logos when available
- [ ] 7.2 Add "Book My Free Discovery Call" CTA to footer
- [ ] 7.3 Verify BV O case study link and image
- [ ] 7.4 Add LinkedIn Company Page link in footer
- [ ] 7.5 Add trust badge section (NL-based, GDPR-compliant, EN+NL)

### PHASE 8 — Final QA & Testing
**Owner:** Dev | **Goal:** Everything verified live before launch signal

- [ ] 8.1 Mobile testing (iOS Safari, Android Chrome) — confirm no horizontal scroll
- [ ] 8.2 Core Web Vitals check via PageSpeed Insights
- [ ] 8.3 Accessibility audit via axe DevTools or WAVE
- [ ] 8.4 Form testing (contact, newsletter — when Web3Forms key applied)
- [ ] 8.5 Multi-browser test (Chrome, Firefox, Safari)
- [ ] 8.6 SEO smoke test (canonical URLs, meta tags, schema)
- [ ] 8.7 Final deploy to production

---

## EXECUTION LOG
| Phase | Task | Owner | Status |
|-------|------|-------|--------|
| 1 | Visual foundation (design system) | Dev | Pending |
| 2 | Hero + CTA optimization | Dev | Pending |
| 3 | Performance fundamentals | Dev | Pending |
| 4 | Accessibility + legal | Dev | Pending |
| 5 | SEO + structured data | Dev | Pending |
| 6 | Content + messaging | Marketing | Pending |
| 7 | Trust + social proof | Marketing+Dev | Pending |
| 8 | Final QA | Dev | Pending |
