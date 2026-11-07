---
title: Troubleshooting
nav_order: 10
---

# Troubleshooting

## Flashing
**No port appears when I plug the board in.**
Almost always the cable or a hub. Use a USB **data** cable (many are
charge-only) plugged **directly** into the computer, not through a hub or
dock. Try another cable before installing drivers.

**Upload fails with "No more data to read" or times out.**
Set **Tools → Upload Speed** to **115200**. Faster speeds are unreliable on
these boards.

**"Failed to install platform esp32".**
You probably have the ESP32 boards URL listed twice in Preferences. Keep one
copy, restart the IDE, remove the ESP32 platform, then install it once.

**"Sketch too big".**
Set **Tools → Partition Scheme** to **Huge APP**.

**Compile error mentioning WiFiManager callbacks.**
Check you installed **WiFiManager by tzapu** and not a similarly named
library.

## Wi-Fi
**The setup hotspot doesn't appear.**
Hold the button ~5 s and release to clear saved Wi-Fi. The screen will say
**Join hotspot: FlightBoard-setup**.

**It won't join my network.**
The ESP32 only supports **2.4 GHz** Wi-Fi. If your router combines 2.4 and
5 GHz under one name, try enabling a separate 2.4 GHz network.

**I set a static IP and now I can't reach it.**
Hold the button ~5 s to reset Wi-Fi, then set it up again and clear the
static IP fields.

## Data
**No aircraft are showing.**
- Check the location in Settings.
- Try a bigger **Scan size**, or check your altitude filters.
- At night, quiet areas can genuinely be empty.
- Look for a rate-limit notice — you may be out of credits.

**"Rate limited" / it stops updating after a few hours.**
You've used your daily OpenSky credits. Add a free
[OpenSky account](opensky-account.md) or poll less often.

**Route or aircraft type is blank.**
Not every flight is in the public route and aircraft databases.

## Dashboard
**The page won't load.**
Make sure your phone/laptop is on the same Wi-Fi as the board. Hold the
button ~1 s to check the address.

**No sound.**
Tap anywhere on the page first — browsers block sound until you interact —
then check the 🔔 / ♪ buttons.

**"Use my current location" says permission denied.**
Expected on phones — see the [FAQ](faq.md#why-doesnt-use-my-current-location-work-on-my-phone).
Type your town instead.

## Still stuck?
Connect the board to the Arduino IDE and open **Tools → Serial Monitor** at
**115200** baud. The board prints its status there, including how many
flights it found and how much memory is free.
