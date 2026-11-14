# Land Survey Pro — Mobile App

This package converts the supplied Land Survey page into an installable Progressive Web App (PWA).

## Included features
- Create and switch between named surveys
- Capture longitude/easting (X) and latitude/northing (Y) using phone GPS
- Enter X/Y manually
- Save owner name, father's name, land area (acres), date/time and a photo
- Store survey data locally in the browser using IndexedDB
- Export the selected survey to Excel (.xlsx), including photos

## Install on Android
1. Upload the contents of this folder to a web host that serves HTTPS.
2. Open the HTTPS address in Google Chrome on the Android phone.
3. Allow location and camera/photo permissions when prompted.
4. Tap **Install App** if Chrome displays the install option. Alternatively use Chrome menu → **Install app** or **Add to Home screen**.
5. Open Land Survey Pro from the phone's home screen.

## Important deployment notes
- HTTPS is required for service workers and reliable GPS access. `localhost` is allowed for development.
- The first visit should be online so the app shell and ExcelJS library can be cached. Excel export can then work offline after ExcelJS has loaded once.
- Records are stored on that device/browser only. Clearing browser/site data or uninstalling in some browser configurations may remove local records. Export and back up records regularly.
- No server or cloud synchronization is included.
- This is an installable PWA package, not a signed Android APK. A native APK / Play Store release requires an Android wrapper, signing key and build process.

## Local testing
Serve this folder from an HTTPS development host, or use `localhost`:
`python -m http.server 8000`
Then open `http://localhost:8000` on the same computer. For phone testing, use an HTTPS host.
