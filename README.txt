# 9U Draft Board (PWA)

Single-page, offline-capable app for grading 9U tryouts with separate Pitcher/Catcher modules.

## Files
- `index.html` — the entire app + service worker registration
- `sw.js` — service worker for offline caching
- `manifest.webmanifest` — PWA manifest
- `icon-512.png`, `icon-192.png`, `apple-touch-icon.png` — icons

## Deploy to GitHub Pages
1. Create a repo, e.g. `9u-draft-board`.
2. Add ALL files above to the **root** of the repo.
3. In **Settings → Pages**:
   - **Source**: *Deploy from a branch*
   - **Branch**: `main` (or `master`), **Folder**: `/ (root)` → **Save**
4. Your site will be available at: `https://<your-username>.github.io/9u-draft-board/`

## iPhone install
1. Open your GitHub Pages URL in **Safari**.
2. Tap **Share** → **Add to Home Screen**.
3. It will be **offline ready** after the first load.

## Backups
- Use **Quick Backup** in the footer to download your data as JSON.
- Use **Import JSON** in the Players tab to restore.

## Notes
- All data is stored locally on the device via `localStorage`.
- Avoid Private Browsing in Safari, which clears storage more aggressively.
