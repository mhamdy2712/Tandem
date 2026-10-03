# Install guide

Tandem has two parts: an app for your **Windows PC** and an app for your **Android phone**. You install the PC part first; it then gives you the phone part.

- [On the PC](#1-install-tandem-on-your-pc)
- [On the phone](#2-install-the-android-app)
- [Pair them](#3-pair-the-phone-and-the-pc)
- [Verifying your download](#verifying-your-download)
- [Updating and uninstalling](#updating-and-uninstalling)

## 1. Install Tandem on your PC

1. Download **[Tandem-Setup.exe](https://github.com/mhamdy2712/Tandem/releases/latest/download/Tandem-Setup.exe)**.
2. Run it and press **Install**. It installs into your own user folder, adds a Start menu shortcut (and a desktop shortcut if you leave the box ticked) and starts Tandem.
3. If an older version is running, the installer closes it first.

### If Windows shows "Windows protected your PC"

This appears for any new program that is not signed with a paid certificate.

1. Click **More info**.
2. Click **Run anyway**.

You only do this once per download. You can check the file first, see [Verifying your download](#verifying-your-download).

### If your antivirus asks about a network connection
Tandem listens for your phone on your local network. Windows Firewall may ask whether to allow it: choose **Private networks**.

## 2. Install the Android app

Pick whichever is easier.

### A. From the PC app (easiest)
1. In Tandem on the PC, press **Install Tandem on my phone**. A code appears.
2. Scan it with your **phone's camera app**. The phone opens a page that is served by your own PC, so nothing is downloaded from the internet.
3. If nothing happens when you tap **Download**, the page is probably open inside another app. Open it in **Chrome** instead (menu → *Open in Chrome*), or type the address shown under the code into Chrome.
4. Open the downloaded `Tandem.apk`.

### B. Download the APK directly
Download **[Tandem.apk](https://github.com/mhamdy2712/Tandem/releases/latest/download/Tandem.apk)** on the phone and open it.

### Android will ask a few things

| Android shows | What to do |
|---|---|
| *"For your security, your phone isn't allowed to install unknown apps from this source"* | Tap **Settings**, switch on **Allow from this source** for your browser (once), then go back. |
| *Google Play Protect: "App scan recommended" or a warning* | Tap **More details**, then **Install anyway**. Tandem is not on Google Play, which is why it asks. |

## 3. Pair the phone and the PC

1. Open **Tandem** on the phone. A short setup asks for what the app needs, **one step at a time, with the reason for each**. Only the camera is required (it scans the pairing code); you can skip the rest and allow them later.
2. In the PC app you see a pairing code (**Pair your phone and PC once**). On the phone tap **Pair** and point the camera at it.
3. When it says **Paired**, you are done. From now on the two reconnect on their own whenever both are on the same Wi-Fi, and through the relay when you are away.

The code changes every two minutes and works once. If it expires, press **New code**.

### Adding another phone or PC
- **Another phone to the same PC:** in the PC app, click the phone card at the bottom of the sidebar and choose **Add phone**.
- **Another PC to the same phone:** open Tandem on the phone and add the PC from the PC menu on the home screen.

## Verifying your download

Every release lists the **SHA-256** of each file. To check a file in PowerShell:

```powershell
Get-FileHash .\Tandem-Setup.exe -Algorithm SHA256
Get-FileHash .\Tandem.apk -Algorithm SHA256
```

The value must match the one in the release notes. If it does not, do not run the file.

## Updating and uninstalling

- **Update the PC app:** run the newest `Tandem-Setup.exe`. It replaces the old version and keeps your pairings and settings.
- **Update the phone app:** install the newest `Tandem.apk` over the old one. Your pairings stay.
- **Uninstall the PC app:** Windows **Settings → Apps → Installed apps → Tandem → Uninstall**.
- **Uninstall the phone app:** press and hold the Tandem icon → App info → Uninstall.
- To remove a pairing without uninstalling, use **Forget phone** on the PC, or **Forget** on the phone.
