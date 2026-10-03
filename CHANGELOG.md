# Changelog

All notable changes to Tandem. The newest version is first. Versions follow `major.minor.patch`.

## 1.0.1 — October 2026

### New
- **Chat attachments.** Send pictures and files in the chat, in both directions, with progress. Pictures show in the conversation and open full screen (pinch, drag, double-tap to zoom, share, save). Other files appear as a card you can open, show in its folder or save elsewhere.
- **Choose where received files go** (PC): a folder picker on the Chat page.
- **Pause / Resume** on both sides. A button on the phone (and a notification action) and one on the PC stop all connections until you resume. The PC tells you when a phone is paused.
- **First-run setup on the phone**: permissions are requested one at a time, each with the reason, and you can skip the optional ones.
- **Sleep awareness.** When the PC goes to sleep or hibernates it tells the phone first, so the Wake button shows at once.
- **Install the phone app from the PC.** The PC app shows a code that opens an install page served from your own PC on your local network.
- **Stop sharing from the phone.** The *Phone Screen* tile switches to *Stop sharing* while the phone screen is shared.
- **Phone screen on the PC is view-only** in this version.
- **Better PC screen on the phone**: two-finger pan, + and − zoom buttons, up to 6× zoom; when the keyboard opens the view moves to the place you clicked and a bar above the keyboard shows what you are typing.
- **Stays connected with the screen off.** Wi-Fi is kept awake while Tandem runs, and a card on the phone's home screen explains and fixes what makes Android cut the connection: Battery Saver, battery optimisation, background restrictions, and the auto-launch settings of OPPO, realme, OnePlus, Honor, Huawei, Xiaomi, Samsung and Vivo phones.
- **Chat on the phone looks like a chat.** Files are cards with a type icon, name, size and an Open button; pictures open full screen with zoom; days are separated with Today and Yesterday.
- **Faster over the internet.** The PC screen uses a smaller, lighter picture (1280×720, about 1.8 Mbit/s, 30 fps) when the phone is away from your Wi-Fi.

### Fixed
- After switching a PC on remotely, the PC app could stay on *Starting* and never look for the phone. (A timer that failed when Windows had just started.)
- The phone could keep showing *Connected* after the PC was shut down or lost its network, and the Wake button did not appear. The connection is now dropped when the PC goes silent and the screen updates.
- *Connected · internet* could stay on screen after the phone had moved back to Wi-Fi.
- Layout of the pairing screen and the install page.

### Changed
- Android 16 KB page-size compatibility (updated camera library).
- Removed two Android permissions that make Google Play Protect block sideloaded apps (Accessibility service and notification access). This means **controlling the phone's screen from the PC** and **mirroring phone notifications to the PC** are not available in this version. See the [roadmap](docs/ROADMAP.md).

## 1.0.0 — October 2026

First public release.
- Phone as PC webcam with a virtual camera.
- PC screen on the phone with touch control, multi-monitor and rotated screens.
- Remote Start: Wake-on-LAN, wake stations, away-from-home wake through the relay, auto sign-in.
- Power, volume and media controls; launcher with icons; PC monitoring.
- Files in both directions (files and folders), shared clipboard, notes and links chat.
- Find my phone, optional location sharing.
- Many phones to one PC and one phone to many PCs.
- Security: end-to-end encryption, keys sealed with DPAPI and Android Keystore, per-phone permissions, audit log, optional app PIN.
- Windows installer and Android app.

