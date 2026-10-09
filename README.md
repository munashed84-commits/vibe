# VIBE: hosting guide

Files: `index.html` (the whole app), `sw.js` (offline support), `_headers` (Netlify security headers), `netlify.toml`, `robots.txt`, `404.html`.
Everything is static. No build step, no server, no API keys.

## Option 1: Netlify (easiest)
1. Go to app.netlify.com/drop
2. Drag this whole `vibe-site` folder onto the page.
3. Netlify gives you an https:// link. Done.

## Option 2: GitHub Pages
1. Create a new public GitHub repo and upload all files in this folder to the root.
2. Repo Settings > Pages > Deploy from branch > `main` / root > Save.
3. Your site appears at https://YOUR-USERNAME.github.io/REPO-NAME/

## Option 3: Cloudflare Pages / Vercel
Create a project, choose "static / no framework", build command empty, output directory `.`

## Important
- Must be served over HTTPS for camera recording, the service worker and installing as an app.
- This is a front-end demo: accounts, videos and messages stay in each visitor's own browser. Nobody sees anyone else's content, and reports are not sent anywhere. Say so on the page you share.
- Real multi-user use needs a backend (auth, database, video storage + CDN, moderation, real-time messaging).
- Test after deploying: sign up, upload a short video, like, comment, open the editor.
