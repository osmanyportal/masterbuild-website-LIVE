# Items requiring owner input

Nothing below blocked this deploy. Each item is something only Osmany Portal can truthfully supply. Until then the site stays accurate rather than invented.

---

## Publishable identity

| Item | Why it matters | Current handling |
|---|---|---|
| Florida PE license number | FBPE lookup, `hasCredential.identifier`, About page | Stated as “confirmed in writing during scope review.” **Do not paste a number until you intend it to be public.** |
| Publishable street address / suite | Google Business Profile, `PostalAddress.streetAddress`, `GeoCoordinates` | Schema uses Miami, FL locality only. **No pin, no invented coordinates.** |
| Google Business Profile URL | `sameAs` | LinkedIn person + company only. |
| Principal photograph | About page trust | No unverified portrait was added. |
| Additional authorized project cards | `/work/` | Five anonymized, source-backed cards. Add names only with written authorization. |
| Additional confirmed testimonials | Homepage quotes | Empty placeholders are hidden. Only confirmed quotes render. |
| Instagram / YouTube | `sameAs` | Added — already linked in the homepage footer. Confirm both URLs still resolve. |

## Operations

| Item | Why it matters |
|---|---|
| Live FormSubmit test from production `/contact/` | Confirm inbox, spam folder, Reply-To, and `[NEW PROJECT]` subject on a real message. Send one `TEST — ignore` from your own email after deploy. |
| FormSubmit activation | If GoDaddy is a new referrer, FormSubmit may email a one-time confirmation the first time the new `/contact/` URL posts. |
| Calendly event still 30 minutes / same URL | Current: `https://calendly.com/osmany-portal-masterbuildconsulting/30min` |
| Stripe Payment Link URLs unchanged | No prices were edited. Confirm each guide still opens the intended SKU. |
| Buttondown list URL | Newsletter remains inside the technical-content journey, not equal-weight with project CTA. |
| Professional liability certificate workflow | About/FAQ already say COI is issued once an engagement is active. Confirm the sentence still matches the policy. |
| Florida Building Code 9th Edition date | `/florida-building-code/` states the scheduled statewide date of **31 December 2026** and tells the visitor to verify. Confirm against floridabuilding.org after any Florida Building Commission change. |
| Fire-protection mill vs coordination | `/fire-protection/` describes MEP-coordinated FP and says hydraulic mill design is scoped in writing. Confirm that sentence still matches how you actually engage. |

## Optional later (not in this ZIP)

| Item | Note |
|---|---|
| Content-Security-Policy | Deferred until live FormSubmit, Stripe, Calendly, Plausible, Buttondown, and Google Fonts are tested under a report-only CSP. |
| Unique OG images per hub | All pages share `/uploads/og-card.png`. Fine. Per-service cards are a design task, not a ranking requirement. |
| Google Search Console property verification | Needed to watch sitemap ingestion and 404s. |
| CrUX / field Core Web Vitals | Requires production traffic. Lab screenshots are not field data. |
| Recertification PE eligibility language | Keep the current boundary unless licensure/authority for County report sealing is confirmed for a specific building. |

## Do not add without a source

- Fabricated “X projects approved” or savings claims
- A Miami-Dade map pin
- A chatbot
- A client portal
- A PE number you have not decided to publish
- A recertification due-date calculator
- A claim that Masterbuild performs Florida’s statewide structural milestone inspection

When you have a number, address, or photo, they can be dropped into the existing schema and About page without restructuring the site.
