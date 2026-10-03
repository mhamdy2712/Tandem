# Remote Start (waking your PC)

Tandem can switch your PC on from your phone, whether you are in the next room or on the other side of the world. This page explains how it works and how to set it up.

## How a wake works

1. You press **Wake PC** on the phone.
2. The phone sends the signal in every way it can:
   - a **Wake-on-LAN "magic packet"** when it is on the same network as the PC;
   - a request through the **relay** to every **wake station** you have set up (a small always-on phone at home that sends the magic packet on your home network) and to the PC's own helper if it is running.
3. The PC starts. **Windows can take 3 to 4 minutes to finish loading**, so the phone keeps waiting for up to about **five minutes**, sending a gentle reminder every 20 seconds (never a flood), and shows a countdown.
4. When Tandem on the PC is up, it connects to the phone on its own. If you turned on *Skip the sign-in screen*, it signs in for you.

If the PC is already on but Tandem is closed, the same request makes Tandem start.

## What works from which state

| PC state | Wake | Notes |
|---|---|---|
| **On, Tandem closed** | Yes | The helper that starts with Windows reopens Tandem. |
| **Sleep** | Yes, with Wake-on-LAN | The PC tells the phone before it sleeps, so *Wake PC* appears immediately. |
| **Hibernate / shut down** | Yes, if your hardware supports Wake-on-LAN from that state | Works on most desktops with a network cable; see the checklist below. |
| **Wi-Fi only PC** | Usually no | Wi-Fi cards rarely support waking the PC. Use a cable. |

## Setup checklist

The **Remote Start** page in the PC app checks these for you and shows a tick for each:

- ✅ **Connected by network cable.**
- ✅ **The network card may wake the PC.**
- ✅ **Magic packet wake-up is on.**
- ✅ **Fast Startup is off.** Windows' Fast Startup turns "shut down" into a half-hibernation that many network cards cannot wake from.

Then, **once, in the PC's BIOS/UEFI** (Windows cannot check this): turn on **Wake on LAN** (also called *Power on by PCI-E* or *PCIe wake*), and turn off **ErP / EuP** if your BIOS has it.

If the page shows a missing tick, you can fix it in **Device Manager → Network adapters → your Ethernet adapter → Properties**:
- **Power Management:** tick *Allow this device to wake the computer* and *Only allow a magic packet to wake the computer*.
- **Advanced:** set *Wake on Magic Packet* to **Enabled**.

## Wake stations

A **wake station** is a small helper that stays on at home so Tandem can wake the PC even when the PC is completely off and cannot hear the relay. An old Android phone plugged in and on your Wi-Fi is enough.

1. In the PC app, **Remote Start → Add a wake station**. A code appears.
2. On the spare phone, scan it with the camera and install **Tandem Station** from the page that opens. (Setup is only served on your local network while the code is on screen.)
3. Open it once. It sets itself up, keeps running, and starts again when the phone restarts.

The PC page shows **1 station online** when it is working.

## Skip the sign-in screen

When on, the PC signs in to Windows by itself after a remote start, so Tandem can start. Tandem asks for your Windows password once, checks it, and stores it protected by Windows (as an LSA secret).

> **Security note.** With this on, anyone who can switch your PC on gets into your account. Keep **BitLocker** or a firmware password on, and keep the PC physically safe.

## Start with Windows
Tandem starts in the tray when you sign in and a small helper watches for wake requests while the app is closed. You can turn this off on the same page.

## Troubleshooting
- **The phone shows "waiting" and the PC never starts:** check the four ticks above, and the BIOS setting. A wake station on the same network gives the best chance.
- **The PC wakes but Tandem does not connect:** wait the full countdown; Windows may still be loading. If you did not turn on *Skip the sign-in screen*, the PC waits at the sign-in screen.
- **It works from sleep but not from shut down:** Fast Startup is on, or the BIOS setting is off.
- More in [TROUBLESHOOTING.md](TROUBLESHOOTING.md).
