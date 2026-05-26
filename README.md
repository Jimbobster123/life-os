# Life OS — Setup Guide

## What's in this folder
- `index.html` — your full dashboard app
- `manifest.json` — makes it installable as iPhone app
- `sw.js` — service worker (offline support, fast loads)
- `data.json` — your data (for future Cowork automation)
- `icon.svg` — app icon

---

## Step 1: Create GitHub repo

1. Go to github.com and sign in
2. Click **New repository**
3. Name it exactly: `life-os`
4. Set to **Public**
5. Click **Create repository**

---

## Step 2: Push these files

Open Terminal in this folder and run:

```bash
git init
git add .
git commit -m "Initial Life OS"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/life-os.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

---

## Step 3: Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under "Source" select **Deploy from a branch**
4. Branch: **main**, folder: **/ (root)**
5. Click **Save**
6. Wait ~2 minutes, then your app is live at:
   **https://YOUR_USERNAME.github.io/life-os/**

---

## Step 4: Install as iPhone app

1. Open Safari on your iPhone
2. Go to: `https://YOUR_USERNAME.github.io/life-os/`
3. Tap the **Share** button (box with arrow)
4. Tap **Add to Home Screen**
5. Name it "Life OS" → tap **Add**

It now lives on your home screen and opens fullscreen like a native app.

---

## Step 5: Update the app anytime

Whenever you want to add a feature or update your data:
1. Edit the files (Claude can do this for you)
2. Run:
```bash
git add .
git commit -m "update"
git push
```
3. GitHub Pages auto-deploys in ~60 seconds
4. Refresh on your phone — done

---

## Future: Cowork automation (Phase 2)
- Cowork will watch `data.json` and update it automatically
- Health Auto Export will push Apple Health data into the file
- The dashboard will read live data instead of local state
