---
title: How it works
nav_order: 7
---

# How it works

## The short version
Your Flight Board asks the OpenSky Network, every minute or so, "which
aircraft are inside this patch of sky?" It works out how far away each one
is and where it's heading, then shows them on its screen and on a web page
it hosts itself.

```
 Aircraft ──ADS-B radio──▶ OpenSky receivers ──▶ OpenSky Network
                                                    │  (internet)
                                                    ▼
                                   Flight Board (ESP32, your Wi-Fi)
                                      │                 │
                                   OLED screen     Web dashboard
                                                  (your phone / laptop)
```

## Where the data comes from
Most aircraft broadcast their position, altitude and speed by radio
(ADS-B). Volunteers around the world run receivers that pick these up and
send them to the OpenSky Network. Flight Board reads OpenSky's live
"state vectors" — it does **not** have a radio receiver of its own.

Extra details are looked up only when you open a flight:
- **Airline** — from the callsign prefix (e.g. `EIN` → Aer Lingus), built in.
- **Route** (from → to) — from [adsbdb.com](https://www.adsbdb.com).
- **Aircraft** (registration, type, operator) — from OpenSky's aircraft
  database.

## Your patch of sky
You set a location and a **scan size**. The board asks OpenSky for a box
`scan size` degrees either side of you (default 0.6° — roughly 65 km north–
south). With **radial scan** on, it trims that box to a circle.

Each aircraft is then:
1. filtered by your altitude limits and the "hide aircraft on the ground"
   setting,
2. given a distance from you,
3. given a **closest approach** — assuming it keeps its current heading and
   speed, how many minutes until it's nearest to you, and how close it gets,
4. sorted nearest first (up to 30 aircraft are kept).

## The two displays
- **OLED:** shows one flight at a time. Long text scrolls on the top line.
- **Web dashboard:** the board serves a web page at its own address. The page
  refreshes its data from the board every 5 seconds; the board itself
  refreshes from OpenSky at the poll interval you set (default 60 s).

## Settings and storage
All settings are saved in the ESP32's own flash memory and survive power
cuts and reboots. A few browser-only preferences (sound on/off, traffic
history) are saved in your browser instead. See [Settings](settings.md).

## Limits worth knowing
- OpenSky limits how often you can ask. Without an account you get about
  400 requests a day; with a free account, about 4,000. See
  [OpenSky account](opensky-account.md).
- Coverage depends on OpenSky's volunteer receivers nearby. Low-flying
  aircraft far from a receiver may not show up.
- Aircraft that don't broadcast ADS-B (some military, some light aircraft)
  won't appear.
