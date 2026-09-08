# FULL site ZIP — wipe public_html, then extract this

**File:** `GODADDY-UPLOAD-masterbuild-website-LIVE.zip` (~10 MB)

Complete production site. 398 files + folders. Includes homepage, all hubs, field tools, contact, Daily Code Talk posts, uploads/PDFs, vendor JS, `.htaccess`.

## GoDaddy (empty folder, then extract)

1. Download `GODADDY-UPLOAD-masterbuild-website-LIVE.zip` from this repo (file download icon, not Code → Download ZIP).
2. File Manager → `public_html`.
3. Enable **Show Hidden Files**.
4. Delete everything currently in `public_html` (the site will be down until extract finishes).
5. Upload this zip into the empty `public_html`.
6. Check **Overwrite existing files**.
7. Select the zip → **Extract** into `public_html` (the current folder). Wait until it finishes. Do not close the window.
8. If a folder named `GODADDY-UPLOAD-...` was created, open it, select all, move everything up into `public_html`, delete the empty folder.
9. Confirm `.htaccess`, `index.html`, `field-tools`, `css`, `js`, `about`, `contact`, `daily-code-talk`, `uploads`, `vendor` are all directly inside `public_html`.
10. Delete the zip.
11. Visit:
    - https://masterbuildconsulting.com/
    - https://masterbuildconsulting.com/field-tools/
    - https://masterbuildconsulting.com/contact/
    Hard-refresh (Ctrl+F5).
