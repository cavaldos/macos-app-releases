# macos-app-releases

Sparkle update feeds for cavaldos' macOS apps, served by GitHub Pages.
Each app has its own folder; the app's `SUFeedURL` points at its `appcast.xml`.

| App | Feed |
| --- | --- |
| [Ice](https://github.com/cavaldos/Ice) | https://cavaldos.github.io/macos-app-releases/ice/appcast.xml |
| [Lumio](https://github.com/cavaldos/Lumio) | https://cavaldos.github.io/macos-app-releases/lumio/appcast.xml |
| [Thorion](https://github.com/cavaldos/Thorion) | https://cavaldos.github.io/macos-app-releases/thorion/appcast.xml |

Release CI writes these files. Don't edit them by hand.

## Adding an app

1. Set `SUFeedURL` in the app's Info.plist to `https://cavaldos.github.io/macos-app-releases/<app>/appcast.xml`.
2. Have its release script run `generate_appcast` and push the result to `<app>/appcast.xml` here.
3. Give the app repo the `MACOS_APP_RELEASES_DEPLOY_KEY` secret (write deploy key on this repo).
