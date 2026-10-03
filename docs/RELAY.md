# The relay (away from home)

At home your phone and PC talk **directly** over Wi-Fi. When you are away, your phone and your home PC usually cannot reach each other (routers and carriers block incoming connections), so Tandem uses a **relay**: a small server on the internet that both sides connect *out* to, and that passes the traffic between them.

## What the relay does
1. The phone connects to the relay and waits.
2. When the PC wants to reach the phone (or the phone wants to wake the PC), the PC connects to the same "room" on the relay.
3. The relay joins the two connections together and forwards bytes in both directions.

The room name is derived from your pairing secret, so only your own two devices know which room to use. Nobody can find your room by guessing.

## What the relay can and cannot see

| It **cannot** see | It **can** see |
|---|---|
| Your files, screen, camera, clipboard, chat and commands: all of it is encrypted end to end between your phone and your PC with keys the relay never has. | That a connection exists, its **IP addresses**, **when** it happens, and **how much data** moves. |

The relay does not store anything: no logs of content, no files, no accounts. It limits how fast anyone can knock on it (to keep it available) and how many rooms exist.

## Home first
Tandem always tries the **local network first**. The relay is only used when the direct path fails, and if the phone comes back onto your Wi-Fi while connected through the relay, Tandem switches to the direct path on its own.

## Speed
Traffic through the relay is slower than your Wi-Fi, because it goes up from your home internet connection, through the relay, and down to your phone. To keep it usable, the PC screen automatically uses a lighter picture (720p, about 1.8 Mbit/s, 30 fps) when the phone is connected through the relay.

## Turning it off
If you prefer that nothing ever leaves your home network, switch **Away from home** off in the PC app under **Remote Start**. Tandem then works only on the local network, and waking the PC from outside stops working too (wake stations also use the relay).

## Who runs it
The relay used by Tandem is run by the author. It does not require an account and does not identify you.
