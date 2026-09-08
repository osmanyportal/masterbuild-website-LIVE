# Changelog — Masterbuild Consulting production, September 2026

Production optimization of the existing GoDaddy static site. Not a rebuild. Not a framework migration.

---

## Pass 3 — 8 September 2026 (this ZIP)

Additional technical, field, marketing, and conversion work on the same static GoDaddy architecture. No invented PE number, street address, case outcomes, chatbot, or framework migration.

### Intake bug fix (production)

Project-type options for healthcare, garage, loads, and combustion air had been inserted into the **Role** dropdown on `/contact/`. They now live under **What do you need Masterbuild to do?**, with plumbing and fire-protection coordination added. Query-param prefill (`?type=garage|plumbing|fire|…`) and the “what to send” hint both resolve against the correct select.

### Field tools (`/field-tools/`) — now eight helpers

| Tool | Basis | What it returns |
|---|---|---|
| Kitchen Type I / Type II pathfinder | IMC 505–508 | Classification, not a hood determination |
| Outdoor-air occupancy estimator | IMC Table 403.3.1.1 (2024 model) | Breathing-zone Vbz only |
| Enclosed-garage estimator | IMC 404 / Daily Code Talk #38 | Full-On 0.75 cfm/sf and Standby 0.05 cfm/sf |
| Combustion-air method check | IMC Ch. 7 educational rates | Indoor volume / two-opening / one-opening / mechanical / listing |
| Kitchen makeup-air equality check | IMC 508 | Exhaust vs identified makeup; transfer air is not assumed |
| Fire/smoke damper pathfinder | IMC 607 | Assembly type → likely damper; not a listing selection |
| Comment classifier | Live review patterns | Hub + what to send |
| Recertification records pack | Published readiness checklist | Copyable send-list. **Not a due-date calculator.** |

Spanish entry: `/herramientas-de-campo/` (same tools, Spanish framing, `/contacto/` intake).

### New hubs (corpus-backed or practice-critical)

| URL | Why it exists |
|---|---|
| `/florida-building-code/` | 8th Edition (2023) currently in force; 9th Edition scheduled 31 Dec 2026; Daily Code Talk teaches 2024 IMC as preparation, not as the review standard for a live 8th-Edition set |
| `/typical-plan-review-comments/` | Educational library of comments that actually appear — not an approval promise |
| `/what-to-send/` | Share-link checklist by job type |
| `/electrical-vs-structural-recertification/` | County electrical path ≠ Florida structural milestone inspection |
| `/plumbing/` | Isometrics, grease, County plumbing checklists, septic/well split |
| `/fire-protection/` | MEP-coordinated FP; hydraulic mill not assumed |
| `/faq/` | Short answers with the same professional boundary |

### Marketing / conversion / UX

- Field tools in primary nav (homepage React nav + static chrome + Spanish “Herramientas”)
- Mobile sticky “Send project background / Call” on every page except `/contact/` and `/contacto/`
- Visual breadcrumbs on new pages
- Print stylesheet for field-tool results
- Homepage Field knowledge grid adds FBC vs IMC, typical comments, plumbing, what to send
- DCT related-hub strip now points at the 404 estimator, 607 pathfinder, combustion-air check, and makeup-air check where the post matches
- 404 recovery links include the new hubs

### What was still not done (on purpose)

- No PE license number, geo pin, fabricated testimonials, or case outcomes
- No recertification due-date calculator
- No CSP (still deferred until live FormSubmit / Stripe / Calendly / Plausible are tested)
- No unique OG images per hub
- Fire-protection hydraulic design is scoped in writing, not claimed as a mill

---

## Pass 2 — 8 September 2026

Knowledge, marketing, and conversion on top of the 7 September production pass. Still static HTML for GoDaddy. Still no invented PE number, street address, case outcomes, or chatbot.

### Field tools (`/field-tools/`)

Three educational helpers that turn a vague question into a better inquiry:

- **Kitchen Type I / Type II pathfinder** — cooking type → likely IMC 505–508 path. Not a hood determination.
- **Outdoor-air occupancy estimator** — IMC Table 403.3.1.1 educational rates → breathing-zone outdoor air (Vbz = Rp×P + Ra×A). Not system outdoor air, not ASHRAE 170.
- **Recertification records pack** — checklist of the same items as the readiness page. Builds a copyable send-list. **Not a due-date calculator.**

### Technical hubs (corpus-backed)

| URL | Why it exists |
|---|---|
| `/ventilation/` | IMC Chapter 4 — largest DCT cluster + free Ch. 4 PDF |
| `/combustion-air/` | IMC Chapter 7 + paid Ch. 7 guide |
| `/duct-systems/` | IMC Chapter 6 + 607 damper comments |
| `/parking-garage-ventilation/` | IMC 404 — Miami podiums |
| `/healthcare-ventilation/` | IMC 407 / ASHRAE 170 — not Table 403 |
| `/hvac-load-calculations/` | IMC 312 + existing Florida checklists |
| `/tenant-improvement-mep-miami/` | Highest-volume commercial permit type locally |
| `/mejoras-de-locales-mep-miami/` | Spanish TI |
| `/permit-comment-response/` | Highest-intent conversion path |

### Marketing / audience

- `/for-architects/`, `/for-owners/`, `/for-contractors/`
- `/contacto/` — full Spanish intake (same FormSubmit, `[NEW PROJECT]` subject, honeypot, native fallback)
- Homepage **Field knowledge** grid (EN/ES)
- Spanish hero/nav CTA → `/contacto/`
- `llms.txt` for AI-search citation
- Organization `sameAs` now includes Instagram and YouTube (already in the homepage footer)
- Daily Code Talk posts (251) load a contextual hub strip before the existing CTA

### Intake

New `?type=` keys: `ventilation`, `healthcare`, `garage`, `load`, `combustion`, `ducts` (plus existing `ti`, `kitchen`, `comments`, `recertification`, …). Dynamic option insert if the select does not yet contain the mapped label.

---

## Conversion and qualified intake

- Dedicated `/contact/` intake. Fields cover who, where, jurisdiction, stage, discipline, blocker, documents, deadline, and the actual question.
- Subject line routing, e.g. `[NEW PROJECT] Recertification / Electrical / Miami-Dade County, FL / Under permit review`.
- Document-link field (Drive / Dropbox / OneDrive / AccuNet). No raw CAD upload — FormSubmit cannot safely accept `.dwg`.
- Honeypot `_honey`. Native POST fallback if the AJAX path fails.
- Query prefill: `/contact/?type=recertification|septic|well|kitchen|existing|mep|comments|advisory|garage|plumbing|fire|…`.
- Contextual “what to send” hint that changes with project type.
- High-intent pages now point the **primary** button at `/contact/` (mailto remains as a secondary path).
- Homepage hero CTA: **Send Project Background**. Secondary: 30-minute scoping call.
- Homepage form: same routing, honeypot, document-link, blocking-issue fields.

## Trust and IA

- `/about/` and `/acerca-de/` — Osmany Portal, PE; Florida-licensed; PE number confirmed in writing (not published).
- `/process/` and `/proceso/` — five steps, fixed fee after scope review.
- `/work/` — verified relationship cards only. No “approved / saved / resolved” claims.
- Empty testimonials hidden. Confirmed quotes only.
- Sixth service: Monthly Design Advisory (the “six ways” list had five items).
- Public brand standardized to **Masterbuild Consulting**. Legal name retained in footers and legal pages.

## Performance

| Payload | Before | After | Status |
|---|---|---|---|
| DCT archive JS | `dct-data.js` 2.9 MB (full bodies) | `dct-index.js` 444 KB (title/summary/tag/hay) | **VERIFIED** lab |
| Article bodies | Inside the 2.9 MB bundle | Static HTML per slug (already existed; now the open path) | **VERIFIED** |
| Archive search | Required the fat bundle | Uses slim index; `801.18` ranks the 801.18 post first | **VERIFIED** in-browser |

`dct-data.js` is omitted from the production ZIP. Rollback still contains it.

Core Web Vitals field data: **REQUIRES POST-DEPLOYMENT DATA** (CrUX / Search Console). Not claimed.

## Search, schema, indexation

- `WebSite` + `SearchAction` → `/daily-code-talk/?q={search_term_string}`.
- `Organization` + `Person` (`hasCredential` Florida PE, no invented license number).
- `Service` provider is `Organization`, not deprecated `ProfessionalService`.
- DCT `BlogPosting.publisher` updated on all 251 posts.
- FAQ JSON-LD only where the page already shows those Q&As.
- `areaServed`: Miami, Miami-Dade County, Florida. **No GeoCoordinates** (no publishable street address on file).
- Sitemap: new canonical URLs added; 404 and utility files not listed.
- `robots.txt`: allow all + sitemap. Sensitive files are excluded from deploy, not hidden by robots.

## Legal / professional boundary

- `/privacy/`, `/terms/`, `/disclaimer/` added.
- Layered disclaimer: short note on technical pages; full page for detail.
- Recertification / septic / well scope boundaries unchanged (readiness ≠ sealed County report; screen ≠ agency determination).
- FBC edition page states the 8th Edition is currently in force and asks the owner/AHJ to confirm the 9th Edition date.

## Accessibility / UX

- Skip link, visible focus, 44px targets on new chrome.
- Form labels on every intake field; inline error text; success state.
- `prefers-reduced-motion` on shared CSS.
- 404 is a recovery tool (hubs + DCT search), `noindex`.
- Mobile sticky CTA; print styles on field tools.

## Security headers (`.htaccess`)

**IMPLEMENTED:** `X-Content-Type-Options nosniff`, `Referrer-Policy strict-origin-when-cross-origin`, `Permissions-Policy` (camera/mic/geo/payment off), `X-Frame-Options SAMEORIGIN`, `X-XSS-Protection 0`, directory listing off, deflate, short HTML cache / longer static cache.

**DEFERRED:** Content-Security-Policy.

## What was not done (on purpose)

- No chatbot, CRM, login, database, or framework migration.
- No invented license number, map pin, case outcomes, or approval rates.
- No recertification due-date calculator.
