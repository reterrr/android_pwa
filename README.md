# Accelerometer PWA (no Android Studio)

The app uses the Web `devicemotion` event to display acceleration including gravity. It does not transmit any sensor values.

## Publish to your phone (GitHub Pages)

1. Create a new public GitHub repository (for example `accelerometer`).
2. Upload all five app files from this directory to the repository root: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, and `icon-512.png`.
3. In the repository, open **Settings → Pages → Build and deployment**.
4. Choose **Deploy from a branch** and select `main` / `(root)`; save.
5. Open `https://YOUR_USERNAME.github.io/accelerometer/` in Chrome on your Android phone.
6. Tap **Start reading**, then Chrome's menu **⋮ → Add to Home screen → Install** (wording can vary).

Motion data requires HTTPS, which GitHub Pages supplies. After the first load, the service worker caches the app for offline use. It only samples while the app is open and active.

## Customize

Modify `index.html` and update the cache version in `sw.js` (for example v2) so existing installations update their cached files.
