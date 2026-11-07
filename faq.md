---
title: FAQ
nav_order: 11
---

# FAQ

### Does it pick up aircraft radio signals itself?
No. It reads live positions from the OpenSky Network over the internet.
OpenSky's data comes from volunteers' receivers.

### Do I need an account or subscription?
No, it works anonymously. A free OpenSky account is recommended so it can
run all day — see [OpenSky account](opensky-account.md).

### Can I see it from outside my home?
Not yet. The dashboard is only on your home network. Remote viewing is
planned.

### Why doesn't "Use my current location" work on my phone?
Phones only share your location with secure (`https://`) pages. The board's
page is a plain `http://` page on your home network, so the phone blocks it
and reports "permission denied" — it isn't a setting you've missed. Type
your town in **Place** instead.

### Why is a plane I can see not on the list?
It may be outside your scan area or altitude filters, not broadcasting
ADS-B, or out of range of OpenSky's receivers (more common for low-flying
aircraft far from a receiver).

### What does "closest approach" mean?
If the aircraft keeps its current heading and speed, how long until it's
nearest to you and how close it'll get. `--` means it's moving away.

### Can I use a different ESP32 board?
Any ESP32 with a 128×64 SSD1306 OLED on pins 21/22 should work. Other pin
layouts and screens are planned — see [Hardware](hardware.md#other-boards).

### How do I update it?
The board tells you when a new version is out (a small arrow on the screen
and a banner on the dashboard). Follow [Update your board](update.md) — it
takes about 3 minutes and keeps your settings. Updating over Wi-Fi with no
cable is planned.
