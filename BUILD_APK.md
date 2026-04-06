# 🚀 CSE 2027 Study App — APK Build Guide

## Option 1: PWABuilder (Easiest — Free, No Coding Required)
1. Host the app on any static hosting (GitHub Pages, Netlify, etc.)
2. Go to https://www.pwabuilder.com
3. Enter your URL → click Start
4. Click "Android" → "Generate Package"
5. Download the `.apk` or `.aab` file
6. Install on Android via "Unknown Sources" OR upload to Play Store

## Option 2: Bubblewrap (Google's Official PWA → APK Tool)
```bash
npm install -g @bubblewrap/cli
bubblewrap init --manifest https://your-domain.com/manifest.json
bubblewrap build
# Output: app-release-signed.apk
```

## Option 3: Capacitor (Ionic — Full Native APK)
```bash
npm install -g @capacitor/cli
npm init
npm install @capacitor/core @capacitor/android
npx cap init "CSE 2027" "com.cse2027.studyapp"
# Copy your files to www/ folder
npx cap add android
npx cap sync
npx cap open android
# Build in Android Studio: Build > Generate Signed Bundle/APK
```

## Option 4: Self-Host & Install as PWA (Easiest on Android)
1. Upload all files to https://netlify.com (drag & drop)
2. Open the URL in Chrome on Android
3. Tap menu → "Add to Home Screen" / "Install App"
4. App installs with icon, fullscreen, offline support
✅ This works 100% offline after first load!

## File Structure
```
studyapp/
├── index.html     ← Main app (100% self-contained)
├── manifest.json  ← PWA manifest
├── sw.js          ← Service Worker (offline + notifications)
└── icons/         ← App icons (all sizes)
    ├── icon-72.png ... icon-512.png
    ├── apple-touch-icon.png
    └── favicon.png
```

## Features Included
✅ Splash Screen
✅ Offline First (Service Worker + IndexedDB)
✅ Push Notifications (Web Notifications API)
✅ Background Notifications via Service Worker
✅ Daily Study Reminders
✅ Streak Tracker + Calendar Heatmap
✅ Session Logger with Timer
✅ Subject-wise Progress Tracking
✅ Analytics Dashboard (Canvas Charts)
✅ Habit Tracker
✅ Cornell Notes
✅ To-Do List with Reminders
✅ Backup/Export JSON + CSV
✅ Full Screen (Standalone mode)
✅ Installable APK via PWABuilder/Bubblewrap
✅ All 8 UPSC Subjects with 200+ Topics
✅ No Internet Required After First Load
✅ Data Persists Permanently (IndexedDB)
✅ Native-like Performance
