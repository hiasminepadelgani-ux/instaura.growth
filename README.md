# Instaura Growth — Prototype

## Included
- Responsive web dashboard for mobile and desktop
- Lead/contact CRUD, search, status filtering
- Campaign planning cards and status toggles
- Workflow recipe builder and status toggles
- Local browser storage and JSON export/import
- PWA manifest and service worker files for installable/offline shell

## Important limitations
This is a prototype, not a production-ready multi-user SaaS. It has no secure login, shared cloud database, tenant isolation, background workflow execution, or real email/SMS/WhatsApp delivery. Demo data is stored locally in the browser. Do not enter sensitive real customer information.

## Run locally
Open `index.html` in a modern browser. Core UI works locally. PWA installation and service worker/offline caching require hosting on HTTPS or localhost.

## Free deployment path
1. Create a GitHub account and a new public repository named `instaura-growth`.
2. Upload `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, and `icon-512.png` from this folder.
3. In repository Settings → Pages, choose deploy from the main branch and root folder.
4. Wait for GitHub Pages to publish the HTTPS site.
5. Open the published site in Chrome on Android → browser menu → Install app / Add to Home screen.
6. Test add/edit/delete lead, create campaign, create workflow, export/import, and offline shell.

GitHub Pages is static hosting; it does not provide a backend or private customer accounts.

## Android / Play Store
The PWA can be installed directly from its HTTPS website without publishing to the Play Store. A Play Store release typically requires a packaged Android app (often via Trusted Web Activity or a native wrapper), store assets, policy compliance, and a Play Console developer account fee. Do not assume Play Store publishing is free.

## Production roadmap
1. Add hosted authentication and database (evaluate free tiers, limits and terms).
2. Enforce tenant/user data separation and server-side authorization.
3. Add email provider integration with verified sender domain, unsubscribe/consent controls, bounce handling, and logs.
4. Implement queued jobs, retries, rate limits, and audit logs.
5. Add subscription billing only after validating demand.
