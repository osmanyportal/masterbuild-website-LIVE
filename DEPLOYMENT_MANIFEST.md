# Masterbuild Consulting — Deployment Manifest
**Package:** `masterbuildconsulting-godaddy-production-2026-09.zip`  
**Baseline:** original production ZIP (`masterbuild-website-LIVE.zip`) frozen as `masterbuildconsulting-ROLLBACK-original-baseline-2026-09.zip`  
**Date:** 7–8 September 2026  
**Host:** GoDaddy Apache (`public_html`)  
**Cache token:** `20260908-prod4`

Upload **only** the contents of `public_html/` from the production ZIP. Do not upload `_docs/`, this manifest, or the rollback archive.

---

## How to upload on GoDaddy

1. Unzip `masterbuildconsulting-godaddy-production-2026-09.zip`.
2. In File Manager, enable **Show Hidden Files** so `.htaccess` is visible.
3. Upload the **contents** of `public_html/` into the live `public_html/` (overwrite matching files; keep existing files that this ZIP does not contain, such as any server logs).
4. Confirm `.htaccess` landed at `public_html/.htaccess`.
5. Visit:
   - `https://masterbuildconsulting.com/`
   - `https://masterbuildconsulting.com/field-tools/`
   - `https://masterbuildconsulting.com/contact/`
   - `https://masterbuildconsulting.com/daily-code-talk/?q=801.18`
6. Send one `TEST — ignore` from `/contact/` using your own email. Confirm inbox, spam, Reply-To, and `[NEW PROJECT]` subject.

Rollback: unzip `masterbuildconsulting-ROLLBACK-original-baseline-2026-09.zip` and replace `public_html` with that archive’s `public_html/`.

---

## Baseline (original production ZIP)

| Metric | Count / size |
|---|---|
| Files | 351 |
| HTML | 268 |
| JS | 17 |
| CSS | 0 (all CSS was inline) |
| PDF | 49 |
| Images | 15 |
| Bytes | 20,318,394 (~19.4 MB) |
| Daily Code Talk posts | 251 static HTML + SPA archive |
| Largest JS | `dct-data.js` 2,990,059 bytes (bodies of all articles) |

**Integrations (unchanged):** FormSubmit → `osmany.portal@masterbuildconsulting.com`, Stripe Payment Links, Calendly 30-min scoping, Buttondown, Plausible (`data-domain=masterbuildconsulting.com`), LinkedIn.

**Architecture (unchanged):** static HTML for GoDaddy; React 18 production build on homepage / DCT archive / resources / glossaries (no Babel in production); bilingual EN/ES.

---

## Production tree (this ZIP)

| Metric | Count / size |
|---|---|
| Files in working tree | 399 |
| Files in `public_html/` of this ZIP | 398 (`dct-data.js` excluded) |
| HTML | 304 |
| JS | 22 (plus exclusion of `dct-data.js`) |
| CSS | 1 shared (`css/mb-chrome.css`) |
| PDF | 49 (all retained) |
| Images | 19 |
| Intentional exclusion | `dct-data.js` (2.9 MB) — unreferenced at runtime; retained in rollback only |

No original HTML, PDF, image, glossary, Spanish page, or product file was removed.

---

## ADD this pass (Pass 3)

| File | Reason |
|---|---|
| `field-tools/index.html` | Regenerated: eight educational tools + TOC |
| `herramientas-de-campo/index.html` | Spanish field-tools entry |
| `florida-building-code/index.html` | FBC 8th vs 9th vs teaching IMC |
| `typical-plan-review-comments/index.html` | Comment library |
| `what-to-send/index.html` | Intake checklist by job type |
| `electrical-vs-structural-recertification/index.html` | County electrical ≠ statewide structural |
| `plumbing/index.html` | Plumbing hub + County checklists |
| `fire-protection/index.html` | FP coordination (not a mill claim) |
| `faq/index.html` | Aggregated FAQ + JSON-LD |

## CHANGE this pass

| File | Reason |
|---|---|
| `js/mb-tools.js` | Garage 404, combustion air, makeup 508, 607 dampers, comment classifier |
| `js/mb-intake.js` | `plumbing`, `fire`, `ducts`, `damper` type keys + hints |
| `js/mb-track.js` | Mobile sticky CTA (skipped on intake pages) |
| `js/mb-related.js` | DCT posts link to the matching tool |
| `mb-hero.js` | Homepage nav: Field tools / Herramientas |
| `mb-sections.js` | Field knowledge grid expanded |
| `css/mb-chrome.css` | Breadcrumbs, tool TOC, sticky, print |
| `contact/index.html` | Role vs project-type bugfix; new types |
| `contacto/index.html` | Matching project types |
| `.htaccess` | Unchanged this pass (headers already shipped) |
| `sitemap.xml` / `llms.txt` / `404.html` | New URLs |

Cache-bust query on scripts/styles: `20260908-prod4`.

---

## Do not upload

- `_docs/`
- `README-DEPLOY.txt`
- the rollback ZIP
- `dct-data.js`

---

## After upload — owner test

See `POST_DEPLOYMENT_QA.md` and `ITEMS_REQUIRING_OWNER_INPUT.md`.
