---
title: First-time setup
nav_order: 4
---

# First-time setup

## 1. Connect it to your Wi-Fi
The first time it starts (or whenever it can't find a known network), the
board creates its own Wi-Fi hotspot.

1. The screen shows **WI-FI SETUP — JOIN THIS HOTSPOT: FLIGHTBOARD-SETUP**.
2. On your phone, join the Wi-Fi network **FlightBoard-setup**.
3. A setup page opens automatically. (If not, open a browser and go to
   `192.168.4.1`.)
4. Tap **Configure WiFi**, pick your home network and enter its password.
5. The board saves it, connects, and shows its **address** (e.g.
   `192.168.1.42`) with a **QR code** for 10 seconds.

The hotspot stays open for 3 minutes. If nobody sets it up, the board
restarts and tries again.

> The board works on **2.4 GHz** Wi-Fi only.

## 2. Open the dashboard
On a phone, just **scan the QR code** on the board's screen with the camera.
Or, on any phone or computer on the same Wi-Fi, open a browser and go to the
address shown, e.g. `http://192.168.1.42`.

Forgot the address? **Hold the button for about 1 second** and let go — the
address and QR code come back for 15 seconds.

## 3. Set your location
The board starts out watching the sky over Shannon, Ireland.

1. Open **Settings** (the ⚙ next to "Scanning", or the menu).
2. Type your town or city in **Place** and press **Find**, or enter latitude
   and longitude yourself.
3. Press **Save changes**. The board refreshes within a few seconds.

If the place can't be found, nothing is changed and you'll see
"Place not found" — try a nearby larger town, or add the country
("Ennis, Ireland").

"Use my current location" works on laptops, but phones usually block it on
local web pages — see [FAQ](faq.md#why-doesnt-use-my-current-location-work-on-my-phone).

## 4. (Recommended) Add a free OpenSky account
Without an account the board can make about 400 requests a day, which runs
out after a few hours at the default refresh rate. A free account gives
about 4,000 a day. See [OpenSky account](opensky-account.md).

## Next
- [Using the device](using-the-device.md)
- [Web dashboard](web-dashboard.md)
- [All settings](settings.md)
