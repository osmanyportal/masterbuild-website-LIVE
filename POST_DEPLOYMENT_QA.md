# Post-deployment QA — Masterbuild Consulting (Pass 3)

Lab checks run against the packaged static tree before ZIP. Field Core Web Vitals, FormSubmit delivery, and Search Console ingestion require the live host.

---

## Validation actually performed (this pass)

| Check | Result |
|---|---|
| New hubs return 200 on the preview server | `/field-tools/`, `/florida-building-code/`, `/typical-plan-review-comments/`, `/what-to-send/`, `/electrical-vs-structural-recertification/`, `/plumbing/`, `/fire-protection/`, `/faq/`, `/herramientas-de-campo/` — **200** |
| Contact Role vs project-type | Healthcare/garage/loads/combustion **removed from Role**; present under project type. **VERIFIED** in HTML |
| `?type=plumbing` prefills project type + hint | **VERIFIED** in Playwright: value `Plumbing / grease interceptor / isometrics` |
| `?type=garage` prefills | **VERIFIED** (intake page loads; sticky CTA **absent** on `/contact/`) |
| IMC 404 estimator | 12,000 sf automatic → Full-On **9,000 cfm**, Standby **600 cfm**. **VERIFIED** |
| Combustion-air two-opening | 200,000 Btu/h → **50 in²** each (1 in² / 4,000). **VERIFIED** |
| Sticky CTA | Present on hubs and homepage; **not** on `/contact/` or `/contacto/`. **VERIFIED** |
| Horizontal overflow | Desktop 1440 and mobile 390 on new pages: **none** |
| JS syntax | `mb-tools.js`, `mb-intake.js`, `mb-track.js`, `mb-related.js`, `mb-hero.js`, `mb-sections.js` — `node --check` **pass** |
| Console / page errors on Pass 3 pages | **0** (Playwright) |
| `dct-data.js` omitted from production ZIP | **YES** (rollback retains it) |
| Original PDFs retained | **49** |
| Architecture | Static HTML + existing React 18 homepage. **No framework migration** |

Playwright screenshots: `/workspace/screenshots/p3-*.png` (desktop + mobile for new hubs, garage result, combustion result, plumbing intake, home mobile sticky).

---

## Owner must do on the live domain (cannot be faked here)

1. Send a `TEST — ignore` from `https://masterbuildconsulting.com/contact/`. Confirm inbox, spam, Reply-To, and `[NEW PROJECT]` subject. FormSubmit may require a one-time confirmation if GoDaddy is a new referrer.
2. Repeat once from `/contacto/`.
3. Confirm Calendly 30-minute URL still opens.
4. Confirm each Stripe Payment Link on `/resources/` still opens the intended SKU.
5. Submit the updated `sitemap.xml` in Google Search Console.
6. Confirm Instagram and YouTube URLs in the footer still resolve (already in `sameAs`).
7. Confirm the Florida Building Code 9th Edition effective date against [floridabuilding.org](https://floridabuilding.org) before treating 31 Dec 2026 as immovable. The page already says to verify.

---

## Not claimed

- Live FormSubmit delivery
- CrUX / field LCP, INP, CLS
- Search ranking
- Permit-approval rates
- Recertification due dates
- That fire-protection hydraulic mill design is in-house on every job

---

## Visual notes

- A “Grok” / “Remix” pill may appear in **this preview environment only**. It is injected by the preview host, not by the GoDaddy ZIP.
- Logo files with spaces in the filename are unchanged originals; space-free copies exist at `/uploads/logo.png` and `/uploads/logo-white.png`.
