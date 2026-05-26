# Archery Scorer

Score archery targets from photos — fully local, no data leaves your device.

## Features
- Auto-detects arrows using pixel analysis
- Falls back to tap mode if detection fails
- Supports WA Outdoor (1–10), Field (1–6), and Indoor faces
- Flexible arrows per end
- Tap any arrow to correct its score
- Session totals with end-by-end breakdown
- Works offline as a PWA — installable on iOS/Android

## Deploy to GitHub Pages

1. Create a new GitHub repo (e.g. `archery-scorer`)
2. Upload all files from this folder to the repo root
3. Go to **Settings → Pages**
4. Set source to **Deploy from a branch → main → / (root)**
5. Save — your app will be live at `https://yourusername.github.io/archery-scorer`

## Add to home screen (iOS)
1. Open the GitHub Pages URL in Safari
2. Tap the Share button
3. Tap "Add to Home Screen"

## Add to home screen (Android)
1. Open in Chrome
2. Tap the three-dot menu
3. Tap "Add to Home screen" or "Install app"

## How it works

### Auto-detection
1. Scans pixels for the yellow/gold zone to find target centre and radius
2. Looks for dark clusters (arrow shafts) within the target area
3. Scores each cluster based on distance from centre as a fraction of target radius
4. Falls back to tap mode if detection confidence is low

### Tap mode
- If no target is found: tap the gold centre first, then each arrow
- If target found but arrows missed: just tap the missing arrows
- Tap any arrow chip to manually correct its score

## Tips for best detection
- Shoot photo straight-on (not at an angle)
- Good even lighting — avoid harsh shadows across the target
- Dark arrows work best against the coloured target rings
- Photo taken from ~2–3m gives good resolution without distortion

## Files
- `index.html` — the entire app (self-contained)
- `sw.js` — service worker for offline/PWA support
- `manifest.json` — PWA metadata
- `icon.svg` — app icon
