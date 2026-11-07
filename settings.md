---
title: Settings reference
nav_order: 8
---

# Settings reference

Open the dashboard → **Settings**, change what you need, then **Save
changes**. Settings are stored on the board and survive restarts. The board
refreshes within a few seconds of saving.

## Location
| Setting | Default | Range | Notes |
|---|---|---|---|
| Place | *(none)* | town or city | Press **Find** to look it up. If it can't be found, nothing changes and you see "Place not found". |
| Latitude / Longitude | 52.7019, −8.8647 (Shannon) | decimal degrees | Editing these by hand clears the place name. |
| Scan size | 0.6 | above 0.05, below 5 (degrees) | Distance either side of you. 0.6° ≈ 65 km north–south. Bigger = more aircraft, but the same request cost. |
| Radial scan | Off | on / off | Trim the box to a circle of radius ≈ scan size × 111 km. |

## Display
| Setting | Default | Range | Notes |
|---|---|---|---|
| OLED mode | Step | Step / Ticker | Step: button moves on. Ticker: moves on automatically. |
| Units | Metric | Metric (km, m, km/h) · Imperial (mi, ft, mph) · Aviation (km, ft, kn) | Applies to the screen and dashboard. |
| Poll every | 60 s | 10–120 s | How often the board asks OpenSky. See [usage limits](opensky-account.md#how-long-will-my-credits-last). |
| Seconds per flight (Ticker) | 5 s | 2–30 s | Only used in Ticker mode. |

## Alerts & filters
| Setting | Default | Range | Notes |
|---|---|---|---|
| Close-approach alert | 0 (off) | 0–200 km | Beep + LED when a flight will pass within this distance. Once per flight. |
| Mute beep | Off | on / off | Silences the buzzer (including the overhead chime and tick). |
| Soft tick while a plane is overhead | On | on / off | Quiet tick every 5 s while a plane is within 3 km. The entry chime still plays. |
| Status LED alerts | On | on / off | Turns the blue LED patterns on or off. |
| Min altitude | 0 ft | feet | Hide aircraft below this. |
| Max altitude | 60,000 ft | feet | Hide aircraft above this. |
| Hide aircraft on the ground | On | on / off | Hides taxiing / parked aircraft. |

## Network (advanced)
Leave blank to get an address automatically (DHCP). Changes apply after the
board restarts.

| Setting | Default | Notes |
|---|---|---|
| Static IP | *(blank)* | e.g. `192.168.1.50`. Needs Gateway too. |
| Gateway | *(blank)* | Usually your router, e.g. `192.168.1.1`. |
| Subnet | 255.255.255.0 if blank | |
| DNS | Gateway if blank | e.g. `1.1.1.1`. |

If a wrong static IP locks you out, **keep holding the button for 5 s** to reset Wi-Fi.

## Firmware
| Setting | Default | Notes |
|---|---|---|
| Check for firmware updates | On | Twice a day the board checks the Flight Board website for a newer version. If there is one, a small arrow appears on the screen and a banner on the dashboard links to [Update your board](update.md). It never installs anything itself. **Dismiss** on the banner hides the notice for that version. |

The version you're running is shown here, on the boot screen and in the
dashboard footer.

## OpenSky account
Upload the `credentials.json` from your OpenSky account to raise your daily
limit. See [OpenSky account](opensky-account.md).

## Usage
Shows the requests left today (from OpenSky) and roughly how long they'll
last at your current poll interval.

## Saved in your browser, not on the board
| Preference | Where |
|---|---|
| Arrival chime on/off | Top bar 🔔 |
| Ambient audio on/off | Top bar ♪ |
| Traffic history (sparkline) | Automatic |
| "No credentials" reminder dismissed | Automatic |

These are per browser — your phone and laptop remember their own.

## Resetting
- **Wi-Fi only:** keep holding the button until the bar fills (5 s).
- **Everything else:** re-enter settings, or re-install the firmware with
  "Erase all flash" enabled in the Arduino IDE.
