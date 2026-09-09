# GODADDY-UPLOAD-masterbuild-website-LIVE.zip

Complete standalone site (Pass 9). Extract into `public_html`.

Show Hidden Files. **Overwrite existing files** (especially `.htaccess`).

Live issues this package fixes:
- `/contact/` 404s on GoDaddy even though `/contact/index.html` works
- `/about/` stayed stale (PE 95945 never overwrote)

## New folders (deploy even if old files are skipped)
- `/send/` — same intake form (homepage/nav/sticky now point here)
- `/principal/` — current About with PE 95945
- `/grease-duct-termination/` — IMC 506.3.13 (DCT #62)
- `/licencia/` — Spanish PE 95945
- `.htaccess` internally maps `/contact/` → `/send/` and `/about/` → `/principal/`

Still omitted: WASD, forensics/reserve studies, street address.

## Extract
1. Download **this file** (download icon). Not Code → Download ZIP.
2. `public_html` → Show Hidden Files → Overwrite.
3. Extract into `public_html`. Wait.
4. Confirm `.htaccess` mentions `send/index.html`.
5. Visit https://masterbuildconsulting.com/send/ and https://masterbuildconsulting.com/principal/
