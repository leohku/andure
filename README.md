![Andure Logo](./docs/images/banner.png)

# Andure — DevTools for Android Chrome

![Version: v1.0.5](https://img.shields.io/badge/version-v1.0.5-blue)
![License: MIT](https://img.shields.io/badge/license-MIT-green)

> ❗ Andure also works without AdGuard! You can download **Bromite Browser** and inject Andure's persistent userscript into the browser via the settings. Thanks to [@porobertdev](https://github.com/porobertdev) who made the discovery.

Based on [eruda](https://github.com/liriliri/eruda), **andure** dynamically injects web-based DevTools into any website through a local VPN tunnel (using [AdGuard HTTPS filtering](https://adguard.com/en/blog/everything-about-https-filtering.html)), allowing for inspection and debugging similar to desktop Chromium DevTools.

To start DevTools for a website, **simply shake your phone** and a prompt will appear.

To install, follow the [installation](#installation) section below.

## 1-Minute Demo

https://user-images.githubusercontent.com/63468786/142807725-0489edc5-0d50-4245-9d53-7a26079c290c.mov

Visit [https://youtu.be/fVCdcvZ7Cv8](https://youtu.be/fVCdcvZ7Cv8) if the above video cannot be played.

## Features

- Execute JavaScript on page
- Select an element on the page to view its properties
- Inspect incoming and outgoing network requests
- Inspect website source
- Show localStorage, and cookie information
- etc.

See [eruda docs](https://github.com/liriliri/eruda#Features) for more features.

## Installation

1. Download the [andure script](https://raw.githubusercontent.com/leohku/andure/main/scripts/activate-on-shake/devtools.js) from this repo and save it on your phone. (For browsers with `devicemotion` disabled, e.g. Brave, there is [another script](https://raw.githubusercontent.com/leohku/andure/main/scripts/persistent/devtools.js) that shows the DevTools button persistently)
2. Install [AdGuard for Android](https://adguard.com/en/welcome.html) and enable HTTPS filtering.
3. In `Settings > Extensions`, select `+ New Extension` and locate the above script. Press `Add` after confirming the extension details are correct.
4. Open a new tab and visit a page. Shake your device to confirm the DevTool prompt shows. (Might need to reload browser or page a few times)

**Note:** An alternative to AdGuard for script injection is Tampermonkey, but the [Android app](https://play.google.com/store/apps/details?id=net.biniok.tampermonkey&hl=en_US&gl=US) is no longer actively mantained and hence is NOT recommended.

## Limitations

- For websites served on HTTP, DevTools will be initialized automatically on page load since `devicemotion` is disabled by default on most browsers (and hence device shakes cannot be detected).
- DevTools icons not working for sites with Content Security Policy but without `font-src` set.
- DevTools will not be injected on financial websites and websites with sensitive personal data. A list of 1300+ exclusions can be seen [here](https://github.com/AdguardTeam/HttpsExclusions).

## Future Work

- [ ] **Open-source Android app** — Script injection currently depends on AdGuard's app - this imposes certain limitations (see above) and is proprietary code. An open-source Android app replaces the need for a third-party app (and simplifies the installation process).

## Contributing

Please visit the [contributing guidelines](https://github.com/leohku/andure/blob/main/CONTRIBUTING.md) and feel free to join our [discord server](https://discord.gg/qGUXpVBqW5)!
