# Dundalk Smart Delivery — V1.0 Starter

A personal, local-first Progressive Web App starter for iPhone Safari.

## Included
- English dashboard
- Add multiple delivery stops manually
- Local address book and delivery history using IndexedDB
- Duplicate address matching (normalised text)
- Delivery counter and last-delivered date
- JSON backup export/import
- Route-order estimate for up to 8 stops, only after explicit consent
- Opens the ordered stops in Google Maps

## Important limitations
- This is a starter MVP, not a fully tested commercial navigation product.
- Camera capture is a placeholder. On iPhone, use Photos Live Text to copy printed address text. Automatic in-app OCR is not included yet.
- Route optimisation sends entered addresses to the public OpenStreetMap Nominatim geocoder and sends coordinates to the public OSRM demo server. Review their policies and do not send sensitive addresses unless you accept this disclosure.
- Public demo routing is rate-limited, may be unavailable, and does not provide guaranteed live traffic.
- Address records are stored in Safari's local IndexedDB. They are not encrypted by this app. Protect the iPhone with a strong passcode and Face ID, do not share the device, and export backups only to a private location.
- If Safari website data is cleared, local records may be deleted. Export backups regularly.
- Hosting this PWA on GitHub Pages makes the source files public if the repository is public. Do not put real customer data, backups, API keys, or secrets in the repository.
- This app does not track driver location and does not send customer history to a cloud database.

## Publish using GitHub Pages from iPhone
1. Create a GitHub account and a new **public** repository, for example `dundalk-smart-delivery`.
2. In the repository, upload the contents of this ZIP (not the ZIP itself): `index.html`, `styles.css`, `app.js`, `manifest.json`, `sw.js`.
3. Open repository Settings → Pages.
4. Under Build and deployment, choose Deploy from a branch; select `main` and `/ (root)`, then Save.
5. Wait for GitHub Pages to publish. Open the published `https://YOUR-USERNAME.github.io/dundalk-smart-delivery/` address in Safari.
6. Tap Share → Add to Home Screen.

## Security notes
This app is designed to minimise data collection, but a hosted PWA cannot guarantee that website code is tamper-proof or that the device's browser storage is encrypted by the app. Review the source before using real customer data. Keep iOS updated and use a strong device passcode.
