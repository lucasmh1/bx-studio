# BX Studio — Android Ready

Bronx Four Track + Freestyle Sample Cutter + Notes + IRC  
Now optimized as a Progressive Web App (PWA) for Android.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Main app (mobile-optimized) |
| `manifest.json` | PWA install metadata |
| `sw.js` | Service worker (offline cache) |
| `icon-192.png` / `icon-512.png` | App icons |
| `apple-touch-icon.png` | iOS home screen icon |

---

## Option A — Install as App on Android (Easiest)

1. Put the whole `bx-studio` folder on a web server **or** use a simple local server on your computer and access it from the phone on the same Wi-Fi.
2. Open the page in **Chrome** on your Android phone.
3. Tap the menu (⋮) → **“Install app”** or **“Add to Home screen”**.
4. It will appear like a real app (fullscreen, own icon, no browser bar).

> Note: For the “Install app” prompt to appear, the site must be served over **HTTPS** (or localhost).  
> Free easy hosts: GitHub Pages, Netlify, Vercel, Cloudflare Pages.

### Quick test without a server
You can open the `index.html` file directly in Chrome on the phone, but some features (mic permission, install prompt, service worker) are restricted on `file://`.

---

## Option B — Real Android APK (Capacitor)

Do this on a computer (Windows / Mac / Linux):

```bash
npm create @capacitor/app@latest
# Choose name "BX Studio", framework "Other"

cd bx-studio-app
# copy the contents of this folder into the www/ or dist/ directory

npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap init "BX Studio" "com.bxstudio.app"
npx cap add android
npx cap sync
npx cap open android
```

Then in Android Studio build an APK.

---

## Mobile Improvements Made

- Larger touch targets
- Tabs become compact icon + label on phones
- All layouts stack vertically
- Safe-area padding for notched phones
- PWA installable + basic offline support
- **Per-track speed control** on the Four Track (0.25×–3.00×)

---

Just say which path you want next (host it, improve mobile recording, or Capacitor help).
