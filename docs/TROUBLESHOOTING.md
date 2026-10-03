# Troubleshooting

Start with the quick checks, then find your symptom.

## Quick checks
1. **Is it paused?** Look for **Paused** on the phone's home screen and in the PC title bar. Press **Resume**.
2. **Same network?** For a direct connection the phone and PC must be on the same Wi-Fi/router.
3. **Is Tandem running on the PC?** It lives in the system tray. Open it from the Start menu if you do not see it.
4. **Restart both apps.** Close Tandem on the PC from the tray menu and open it again; force-stop and open the phone app.

## The phone and PC will not connect at home

- **Windows Firewall.** The first time, Windows asks whether Tandem may use the network. Choose **Private networks**. If you dismissed it: Windows Security → Firewall & network protection → *Allow an app through firewall* → tick Tandem for **Private**.
- **Network type.** Your Wi-Fi/Ethernet must be set to **Private** in Windows (Settings → Network & internet → your connection → Network profile type).
- **Guest or "AP isolation".** Some routers keep devices from seeing each other (guest networks, "client isolation"). Put both on the main network.
- **VPN.** A VPN on the phone or PC can route local traffic away. Pause it or exclude local network access.
- **Different subnets.** The phone and PC need to be on the same subnet (for example both `192.168.1.x`). Range extenders in "router" mode can split them.
- **The phone's address changed.** Tandem finds the phone again by itself. If it does not, forget and pair again.

## It connects at home but not away from home
- The PC must be **on** and Tandem running (or its Windows helper). Check **Remote Start → Away from home** is on.
- Both sides need internet access. Some work or school networks block unusual outgoing ports.
- If the PC is off, use **Wake PC** and wait for the countdown, see [WAKE.md](WAKE.md).

## "Connected" is stuck or the screen is slow
- Away from home the PC screen uses a lighter picture, so it is not as sharp as on Wi-Fi.
- Check your PC's **upload** speed: a slow home upload limits everything away from home.
- Lower the frame rate (30 instead of 60) on the PC Screen tile.

## Wake PC does nothing
Go through the checklist in [WAKE.md](WAKE.md#setup-checklist): cable, network card setting, magic packet, Fast Startup, and the BIOS option. A wake station at home makes it far more reliable.

## The connection drops when the phone's screen turns off, or when I close the app
Phones save battery by stopping apps in the background. Tandem shows a card on its home screen when it finds the cause on your phone, with a button that opens the right setting. The usual causes:

- **Battery Saver is on.** Turn it off, or keep it on and allow Tandem below.
- **Battery optimisation.** Allow Tandem to ignore it (the card's *Allow* button), or in Android Settings → Apps → Tandem → Battery choose **Unrestricted**.
- **Your phone maker's own power manager.** This is the most common one:
  - **OPPO, realme, OnePlus (ColorOS / OxygenOS):** Settings → Apps → Tandem → Battery usage → **Launch settings**. Turn **Manage automatically** off, then turn on **Auto-launch**, **Secondary launch** and **Run in background**.
  - **Xiaomi, Redmi, POCO:** Security → Permissions → **Autostart**, switch Tandem on. Also set Battery saver for Tandem to **No restrictions**.
  - **Samsung:** Settings → Battery → Background usage limits → remove Tandem from *Sleeping apps*.
  - **Vivo / iQOO:** Settings → Battery → Background power consumption → allow Tandem. Also allow auto-start.
  - **Huawei / Honor:** Settings → Battery → App launch → Tandem → manage manually and allow all three.
- Closing the app from the recent-apps list is fine on most phones. On some it stops Tandem completely; the settings above prevent that.

## The phone says "not on this phone" / "Not saved" for a chat file
That message arrived before the file could be sent, or you were offline when it was sent. Files in chat are only transferred when the phone and PC are connected. Send it again.

## A phone keeps asking for a permission
Allow it in **Android Settings → Apps → Tandem → Permissions**. For location "all the time", choose *Allow all the time*. For background use, set battery to **Unrestricted**.

## Windows or Android warnings when installing
See [INSTALL.md](INSTALL.md). Both are expected for apps that are not from the Microsoft Store or Google Play.

## The virtual camera does not appear in my app
- Make sure Tandem is open on the PC and the phone's camera is **On**.
- Restart the app that should use the camera; some apps only list cameras when they start.
- Pick **Tandem Camera**.

## Still stuck?
[Open an issue](https://github.com/mhamdy2712/Tandem/issues/new/choose) and include:
- the Tandem version on the PC and on the phone,
- your Windows and Android versions,
- what you tried and what you saw (a screenshot helps),
- whether it happens at home, away from home, or both.

Or write to **mhamdy2712@gmail.com**.
