FAMILY MEAL PLANNER — GITHUB PAGES & MAC MINI PWA BUNDLE
=========================================================

FILES INCLUDED:
- index.html    : Your complete Family Meal Planner app (with offline fallback CSS)
- manifest.json : Android / Foldable Web App Manifest (relative paths for GitHub Pages)
- sw.js         : Offline Service Worker (Network-First on Wi-Fi, Cached when in stores)
- icon-192.png  : 192x192 PNG app icon required by Android's WebAPK installer
- icon-512.png  : 512x512 PNG app icon required by Android's WebAPK installer
- icon.svg      : Vector app icon
- .nojekyll     : Tells GitHub Pages to serve files directly with zero build delay
- Caddyfile     : Optional local Mac mini server config (Port 21110)

---------------------------------------------------------
HOW TO DEPLOY ON GITHUB PAGES (FOR MOTOROLA RAZR & VERSIONING)
---------------------------------------------------------
Option A — Drag & Drop in Your Browser (No Terminal Needed, 60 Seconds):
1. Go to https://github.com/new and create a new repository (e.g. `meal-planner`).
   - Note: Free GitHub Pages works on Public repositories (your actual meal plans and notes are stored in your phone's localStorage, NOT in the repository).
2. Click "uploading an existing file" on the setup screen.
3. Drag all the files from this unzipped folder into the GitHub upload box and click "Commit changes".
4. In your repository, go to: Settings -> Pages (on the left sidebar).
5. Under "Build and deployment" -> "Branch", change "None" to `main` (and `/ (root)`), then click Save.
6. Wait ~30 seconds and visit your new HTTPS link:
   https://<your-github-username>.github.io/meal-planner/

Option B — From Your Mac mini Terminal (With Git Version Control):
1. Unzip this folder on your Mac mini (e.g. ~/meal-planner) and run:
   cd ~/meal-planner
   git init
   git branch -M main
   git add .
   git commit -m "Initial commit: Family Meal Planner v1"
   git remote add origin https://github.com/<your-username>/meal-planner.git
   git push -u origin main
2. Enable GitHub Pages in Settings -> Pages -> Branch: `main` -> Save.

---------------------------------------------------------
INSTALLING ON YOUR MOTOROLA RAZR (STANDALONE + SPLIT SCREEN)
---------------------------------------------------------
1. Delete any old Meal Planner shortcut from your Razr Home Screen first.
2. Open your `https://<your-username>.github.io/meal-planner/` URL in Chrome on your Razr.
3. Tap the purple "📲 Install App" button at the bottom of the page (or Chrome's ⋮ menu -> "Add to Home screen" -> "Install").
4. Because GitHub Pages uses real HTTPS and relative manifest paths with no orientation lock, Android builds a true WebAPK:
   - Opens in full-screen Standalone Mode (no Chrome address bar)
   - Supports Razr Split Screen, Flex View, and External Cover Screen
   - Works 100% offline inside grocery stores!
