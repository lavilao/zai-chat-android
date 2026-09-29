# Z.ai Chat Android wrapper

A lightweight Android WebView wrapper for `https://chat.z.ai/`.

## Build

Requirements: JDK 17 and Android SDK with platform 35 installed. Then run:

```sh
gradle assembleDebug
```

The APK is produced at `app/build/outputs/apk/debug/app-debug.apk`. Debug builds are signed for testing. Release distribution requires your own signing key and release configuration.

## Current behavior

- Opens Z.ai Chat in Android WebView
- JavaScript and DOM storage enabled for the web app
- Android back button navigates WebView history
- Uses the site’s own sign-in and account controls

## Offline chat history

The wrapper currently does not provide offline chat browsing. WebView caching is not a reliable way to preserve conversations: the site may keep chat data server-side, and its scripts/API may require a live connection. A real offline feature should be added only through a supported export/API or user-triggered save, with clear controls to view, export, and delete saved data. Since conversations can be sensitive, local records should be encrypted and excluded from Android backup unless the user explicitly opts in.

## Privacy and scope

This app loads the official Z.ai website and does not claim affiliation with Z.ai. Web content, account behavior, and availability are controlled by that site. The wrapper does not inject credentials, scrape chat history, or bypass site access controls.
