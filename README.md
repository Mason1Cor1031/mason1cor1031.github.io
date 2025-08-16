# 9U Draft Evaluation — PWA

A mobile-optimized, offline-capable Progressive Web App (PWA) for evaluating 9U players.

## Features
- Add/filter/rate players, add notes, export CSV
- Draft rankings generator
- Save/Load progress via LocalStorage
- Installable PWA with offline support (service worker + manifest)

## Getting Started

### Local
1. Serve the folder with any static server (required for service workers). For example with Python:
   ```bash
   python3 -m http.server 8000
   ```
2. Visit `http://localhost:8000` and use **Add to Home Screen** (mobile) or **Install** (desktop Chrome).

### GitHub Pages
1. Create a new repo (or use an existing one) and add these files at the root.
2. Commit & push to `main`.
3. In **Settings → Pages**, set **Source** to **Deploy from a branch**, **Branch** = `main` / root.
4. Wait for the site to build, then visit the provided URL (it must be HTTPS for PWA install).
5. If the app updates, bump `CACHE_VERSION` in `service-worker.js`, commit, and refresh to get the latest.

## Project Structure
```
/
├── index.html
├── manifest.webmanifest
├── service-worker.js
├── offline.html
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Notes
- LocalStorage persists on-device. Clearing browser data will remove saved players.
- Service worker uses **network-first** for HTML and **cache-first** for assets.
