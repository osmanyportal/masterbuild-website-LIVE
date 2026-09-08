# Extract this zip inside GoDaddy public_html

**File:** `GODADDY-UPLOAD-masterbuild-website-LIVE.zip` (~720 KB)

This replaces the previous 10 MB zip. It includes directory entries GoDaddy needs, a safer `.htaccess`, and only the pages that must be updated. It does **not** re-upload Daily Code Talk posts or PDFs already on the server.

## Steps

1. In File Manager, open `public_html`.
2. Enable **Show Hidden Files**.
3. Check **Overwrite existing files**.
4. If you see a leftover `.htaccess` from the last extract, you may overwrite it with this zip.
5. Upload `GODADDY-UPLOAD-masterbuild-website-LIVE.zip`.
6. Select it → **Extract** into `public_html` (not into a subfolder).
7. If extract created a folder named `GODADDY-UPLOAD-...`, open that folder, select all, move everything up into `public_html`, then delete the empty folder.
8. Delete the zip.
9. Confirm these folders exist in `public_html`: `field-tools`, `css`, `js`, `about`, `contact`.
10. Visit:
    - https://masterbuildconsulting.com/
    - https://masterbuildconsulting.com/field-tools/
    - https://masterbuildconsulting.com/contact/
    Hard-refresh (Ctrl+F5).
