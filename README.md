# PrinsGo Admin App

A thin wrapper app — it just opens the hosted admin panel
(https://prinsgo-customer-app.github.io/Prinsgo_admin/) in a full-screen WebView.
No separate login/dashboard code here; all of that lives in the `prinsgo-admin`
static site. This just saves you from running a local server or opening a browser
tab every time.

## If you update the admin panel HTML later
Just push the updated `index.html` to the `Prinsgo_admin` GitHub repo (GitHub
Pages auto-redeploys in ~1 minute). This app doesn't need to be rebuilt — it always
loads whatever is currently live at that URL.

## If the hosted URL ever changes
Edit `ADMIN_PANEL_URL` in `App.js`, then rebuild.

## Setup / build (same pattern as the other two apps)
```bash
cd prinsgo-admin-app
npm install
eas build:configure
eas build -p android --profile preview
```
