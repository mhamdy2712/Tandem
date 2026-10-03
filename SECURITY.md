# Security

Tandem can lock, restart and shut down a PC, browse its files and show its screen, so its security matters. This page explains how it protects you and how to report a problem.

## How Tandem protects you

### Pairing
- You pair a phone and a PC once, by scanning a one-time code shown on the PC. The code changes every two minutes and works only once.
- Pairing creates a secret key known only to those two devices. Nothing is sent to any server during pairing.

### Encryption
- Everything between phone and PC (video, files, clipboard, chat, commands) is encrypted and authenticated with **AES-256-GCM**. Session keys are derived from the pairing secret with **HKDF**, with fresh random values for every connection.
- This also applies when the traffic goes through the internet relay. The relay forwards bytes it cannot read. See [docs/RELAY.md](docs/RELAY.md).

### Keys at rest
- **PC:** the pairing keys are stored with Windows **DPAPI**, tied to your Windows account. Copying the file to another PC or user does not work.
- **Phone:** the keys are sealed with the **Android Keystore**.

### What a phone may do is decided on the PC
Each paired phone has switches on the PC, under **Security**: *Power, Volume and media, Launcher, Files, PC screen, Clipboard,* and *See all drives* (off by default: the phone only sees your own folders). A master switch turns every phone into a view-only device. These checks run **on the PC**, so a modified phone app cannot bypass them.

### Audit log
Sensitive actions (power, launching, file access, screen) and **every blocked attempt** are written to a log you can read in the PC app.

### On the phone
- Optional **app PIN**, stored as a salted hash, with growing delays after wrong tries. While it is on, the app is hidden from screenshots and the recent-apps picture.
- **Pause**: one button on the phone and one on the PC stop all connections until you resume.
- Permissions (camera, location, files...) are requested one at a time, with the reason, and each one can be skipped.

### Wake stations
Setting up a wake station needs a one-time link that is only served on your local network while the setup code is on screen.

## What Tandem does not do
- No account, no cloud storage, no analytics, no advertising, no tracking.
- Nothing is uploaded to the author. Location, files, screen and messages go only to your own paired devices.

## Things you should know
- Anyone who can unlock your phone **while the app has no PIN** can use what that phone is allowed to do. Turn on the app PIN and keep the permissions to what you need.
- If you turn on **"Skip the sign-in screen"** (auto sign-in after a remote start), anyone who can switch your PC on gets into your account. Keep **BitLocker** or a firmware password on.
- Tandem is not yet signed with a paid code-signing certificate, so Windows SmartScreen and Google Play Protect may show warnings. Check the SHA-256 values published with each release.

## Reporting a vulnerability

Please **do not** open a public issue for a security problem.

Email **mhamdy2712@gmail.com** with the subject `Tandem security`, and include:
- what you found and how to reproduce it,
- the Tandem versions of the PC and the phone,
- what you think the impact is.

You will get a reply within a few days. Please give reasonable time for a fix before sharing details publicly. Reports made in good faith are welcome and appreciated.

## Supported versions
Only the latest release receives fixes. Update through the installer or by downloading the newest APK.
