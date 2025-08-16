# 9U Draft Board (PWA)

Single-page, offline-capable app for grading 9U tryouts with separate Pitcher/Catcher modules.

## Files
- `index.html` — the entire app (self-contained UI + logic) + service worker registration
- `sw.js` — service worker for offline caching
- `manifest.webmanifest` — PWA manifest
- `icon-512.png`, `icon-192.png` — app icons (maskable)
- `apple-touch-icon.png` — iOS Home Screen icon

## Deploy to GitHub Pages
1. Create a repo, e.g. `9u-draft-board`.
2. Add ALL files above to the **root** of the repo.
3. In **Settings → Pages**:
   - **Source**: *Deploy from a branch*
   - **Branch**: `main` (or `master`), **Folder**: `/ (root)` → **Save**
4. Your site will be available at: `https://<your-username>.github.io/9u-draft-board/`

> Tip: The service worker scope and `start_url` are relative (`.`), so it works whether you host at the root or under `/9u-draft-board/`.

## iPhone install
1. Open your GitHub Pages URL in **Safari**.
2. Tap **Share** → **Add to Home Screen**.
3. Launch the app from your Home Screen. It will be **offline ready** after the first load.

## Backups
- Use **Quick Backup** in the footer to download your data as JSON.
- Use **Import JSON** in the Players tab to restore or share with assistants.

## Notes
- All data is stored locally on the device via `localStorage`.
- Avoid Private Browsing in Safari, which clears storage more aggressively.
