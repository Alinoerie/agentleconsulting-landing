# AgentleConsulting.com Overhaul — Live Status

## Completed ✅

### Infrastructure
- [x] /book → 200 (was 404)
- [x] /case-study-kitchenware → 200 (was 404)
- [x] All 11 blog posts → 200 (routing fixed via vercel.json)
- [x] Placeholder phone removed from JSON-LD schema
- [x] KvK/BTW placeholders removed from all footers

### Homepage
- [x] Advisory Retainer tier added, Discover tier removed
- [x] "Numerous" → "40+ clients"
- [x] "BV O" cryptic labels → clear plain-English labels
- [x] "See how it works" demoted from competing CTA to plain text
- [x] Amsterdam, NL trust badge added to hero strip
- [x] Schema priceRange updated to current tier names
- [x] Hero headline rewritten: "Stop spending 10 hours a week on work your automation should handle"
- [x] Hero subheading with specific workflow names (inventory, supplier emails, logistics)
- [x] Named methodology: "The Handover-First Framework"
- [x] Dutch tagline: "Vanuit Amsterdam, voor heel Europa"
- [x] "40+ Businesses helped" → "since 2023" on About page

### Pricing Page
- [x] "3–5 workflows" → "4–6 core workflows" throughout
- [x] Transform 6-month minimum label updated
- [x] €500 credit → explicit "Book → proceed within 30 days → €500 deducted" terms
- [x] Urgency signal: "Currently accepting 1 new client per quarter"
- [x] Workflow examples in Automate tier (Amazon–Bol.com sync, supplier RFQ, order-to-ERP, reconciliation)

### Compliance / Technical
- [x] GDPR cookie consent bar (bottom-fixed, localStorage-based)
- [x] FAQ schema on homepage (5 Q&A)
- [x] FAQ schema on pricing page (5 Q&A)
- [x] Accessibility page created (/accessibility.html, WCAG 2.1 AA)
- [x] Mobile: hamburger tap target enlarged to 48px
- [x] Mobile: hamburger z-index fixed (101)
- [x] Mobile: overflow-x hidden on html/body
- [x] Exit-intent Escape key handler confirmed present
- [x] Old gold (#C49A3A) → amber throughout

---

## BLOCKED — Needs Ali

| Priority | Item | Blocker |
|----------|------|---------|
| P0 | Calendly URL for /book.html | Ali — what URL? |
| P0 | Founder photo deploy confirmation | Ali — is founder.jpg cleared to publish? |
| P0 | Testimonial | Ali or Orcha — LinkedIn login-gated |
| P1 | Founder photo on homepage | Dev — waiting on Ali confirmation |
| P2 | LinkedIn Company Page | Ali must create manually at linkedin.com/company/setup/new/ |

### LinkedIn Company Page Setup (Ali — 10 min)
```
URL: https://www.linkedin.com/company/setup/new/
Company name: AgentleConsulting
Website: https://agentleconsulting.com
Size: 1 employee
Industry: Business Consulting / IT Services
Tagline: Automation systems for European SMBs — stop doing busywork, start scaling.
About: Custom automation systems for small and medium businesses across Europe. Based in Amsterdam. Founder: Ali Yasar.
```

---

## Not Started

- [ ] Second case study (needs Ali to provide anonymized client data)
- [ ] Founder story / About page copy rewrite
- [ ] hreflang tags (NL, BE, DE)
- [ ] Image width/height attributes (LCP improvement)
- [ ] Homepage testimonial section (blocked: needs real testimonial)
- [ ] LinkedIn Company Page link in all footers (blocked: page doesn't exist yet)
