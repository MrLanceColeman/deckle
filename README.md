# Deckle static site

These files are ready to upload. They match the paths linked from About in the app:

| File | Intended public path |
| --- | --- |
| `index.html` | `/` |
| `privacy.html` | `/privacy` |
| `terms.html` | `/terms` |
| `support.html` | `/support` |
| `about.html` | `/about` (also shown inside the app) |

**No public hostname is pointed at these files.** Do not treat any URL as live until DNS points at a host that serves this folder.

The app still serves the same files from inside Deckle so About works offline.

## Human upload steps

1. Choose a hostname and a static host. No app server is required.
2. Publish this directory as the site root.
3. Map pretty paths to the HTML files:
   - `/` → `index.html`
   - `/privacy` and `/privacy/` → `privacy.html`
   - `/terms` and `/terms/` → `terms.html`
   - `/support` and `/support/` → `support.html`
4. Point the domain’s records at that host and wait for HTTPS.
5. Open each URL in a private window. Confirm About in Deckle still reaches the same text inside the app even before DNS exists.

Do not add analytics scripts unless you update `privacy.html` first.
