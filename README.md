# Cardano Dev Wallet



## About this Extension

> Built with [Vite](https://vitejs.dev/) + [TailwindCSS](https://tailwindcss.com/) + [WebdriverIO](https://webdriver.io) setup for building and testing extension popup modals, content and background scripts. 

## Development
### Setup

Install dependencies via:

```sh
npm install
```

then start a browser with the web extension installed:

```sh
# run Chrome
npm run start:chrome
```

or

```sh
# run Firefox
npm run start:firefox
```

This will build the extension and start a browser with it being loaded in it. After making changes, Vite automatically will re-compile the files and you can reload the extension to apply them in the browser.

### Build

Bundle the extension by running:

```sh
npm run build
```

This script will bundle the extension as `web-extension-chrome-vX.X.X.crx` and `web-extension-firefox-vX.X.X.zip`. The generated files are in `dist/`.

#### Load in Firefox

To load the extension in Firefox go to `about:debugging#/runtime/this-firefox` or `Firefox > Preferences > Extensions & Themes > Debug Add-ons > Load Temporary Add-on...`. Here locate the `dist/` directory and open `manifestv2.json`

#### Load in Chrome

To load the extensions in Google Chrome go to `chrome://extensions/` and click `Load unpacked`. Locate the dist directory and select `manifest.json`.

### Test

This project tests the extension files using component tests and the extension integration via e2e test with WebdriverIO.

Run unit/component tests:

```sh
npm run test:component
```

Run e2e tests:

```sh
npm run test:e2e
```

## Files:

 - content-script - UI files
 - background.ts - Background script/Service worker
 - index.html - popup UI

If you have any questions feel free to open an issue.
