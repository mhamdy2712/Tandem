# Frequently asked questions

### Is Tandem free?
Yes, for personal use. See the [license](../LICENSE).

### Do I need an account?
No. You pair a phone and a PC by scanning a code. There is nothing to sign up for.

### Does my data go to your servers?
No. Files, screen, camera, clipboard, chat and location go between your own devices, encrypted. The only server involved is the [relay](RELAY.md), and it cannot read anything. You can switch it off.

### Is it really encrypted?
Yes: AES-256-GCM, with keys made when you paired. See [SECURITY.md](../SECURITY.md).

### Why does Windows say "Windows protected your PC"?
Tandem is not yet signed with a paid code-signing certificate, so SmartScreen warns about any new unsigned program. Click **More info → Run anyway**. You can compare the SHA-256 of your download with the one in the release notes first.

### Why does Android / Google Play Protect warn me?
Tandem is installed from a file, not from Google Play. Tap **More details → Install anyway**.

### Is Tandem on Google Play?
Not at the moment.

### Why can't Tandem control my phone's screen or show phone notifications on the PC?
Both need Android permissions (the *Accessibility* service and *notification access*) that make Google Play Protect refuse to install apps that are not from the Play Store. They were removed from this version so it installs normally. They are on the [roadmap](ROADMAP.md).

### Does it work without Wi-Fi?
At home both devices need to be on the same network (the phone can use Wi-Fi and the PC a cable on the same router). Away from home the phone can use mobile data and the PC any internet connection.

### Does it work if my PC is on Wi-Fi?
Yes for everything except waking it when it is off. Wi-Fi cards almost never support that; use a network cable for Remote Start.

### Can I use it with more than one phone or PC?
Yes. See [Features → Several phones and PCs](FEATURES.md#several-phones-and-pcs).

### Can someone else use my PC through Tandem?
Only a phone that has been paired with it. Pairing needs the code that is shown on the PC for two minutes. You decide what each phone may do under **Security**, and the **Pause** button cuts every connection.

### What does it cost in battery and data?
The phone keeps one light connection to be reachable and uses almost nothing when idle. The camera, the PC screen and file transfers use what you would expect; the PC screen is much lighter away from home.

### Which Windows versions are supported?
Windows 10 and 11, 64-bit.

### Which Android versions are supported?
Android 8.0 and newer.

### How do I uninstall it?
See [Install guide → Updating and uninstalling](INSTALL.md#updating-and-uninstalling).

### How do I report a problem or suggest a feature?
[Open an issue](https://github.com/mhamdy2712/Tandem/issues/new/choose), or write to mhamdy2712@gmail.com.
