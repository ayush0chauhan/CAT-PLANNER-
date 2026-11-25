# CAT 2027 Planner (PWA)

No build step, no accounts, no APIs. Files: `index.html` (app), `sw.js` (offline), `manifest.webmanifest`, `icon-*.png`.

## Deploy (pick one)
**Netlify (fastest):** open https://app.netlify.com/drop, drag the `cat-planner` folder in. You get an https URL.

**GitHub Pages:** create a public repo, upload all files to the root, then Settings -> Pages -> Deploy from branch -> `main` / root. URL: `https://<user>.github.io/<repo>/`.

## Install on iPhone
1. Open the URL in **Safari** (not Chrome).
2. Tap **Share** -> **Add to Home Screen** -> **Add**.
3. Launch from the home screen icon. Open it once online; after that it works offline.

## Notes
- Progress is saved in the device's local storage. Use **More -> Export file** weekly (saves via the share sheet, e.g. to Files/iCloud). **Import** restores it.
- Deleting the home-screen app or clearing Safari data erases progress, so keep backups.
- Exam date (default 28 Nov 2027, provisional) is editable under More. It changes the countdown only; the plan is generated for 25 Nov 2026 - 27 Nov 2027.
- Updates: edit files, redeploy. The app refreshes on the next launch or two. Bump `V` in `sw.js` to force a cache reset.
- The plan is generated in code (`tpl()`, `T`, `PH`, `SP` in `index.html`), so you can change phases, topic weights, daily hours or special test dates there. Changing the plan shifts task IDs by date, so back up first.
