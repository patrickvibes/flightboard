---
title: Web dashboard
nav_order: 6
---

# Web dashboard

Open `http://<board-address>/` on any device on the same Wi-Fi. The page
updates itself every 5 seconds — no need to refresh.

## The board
- **Scanning** shows your area and coordinates.
- **Stats line** with the nearest, fastest and highest aircraft.
- **Traffic sparkline** — how many aircraft were in your area over the last
  60 updates, with the peak. Kept in your browser between visits.
- **Flight list** — callsign, distance, altitude (▲ climbing / ▼ descending),
  speed and closest approach, nearest first. The **◉** marker is brightest
  for the closest aircraft and blinks when a flight is new.

**Tap a flight** to open its details: airline, route (from → to) and
aircraft type/registration where known. From there you can:
- **Lock** it to the OLED screen (tap again to unlock),
- **✈ Enter cockpit** for the instrument view.

## Live map
Menu → **Live map**. Aircraft are shown at their positions, pointing the way
they're heading. Tap one to select it.

## Cockpit
A full-screen instrument panel for one flight: airspeed dial, heading
compass and altimeter, updating live. **Exit cockpit** to return.

## Overhead now
When an aircraft comes within **3 km** of you (horizontally), a lime
**OVERHEAD NOW** banner appears at the top of the page and follows that
aircraft. It's brightest when the plane is within about 1.2 km and fades as
it moves away. A rising chime plays as it enters (if sound is on).

The banner follows the board's own live estimate, so it appears at the same
moment as the board's OVERHEAD screen, even between OpenSky updates.

## Sound
Two buttons in the top bar:
- 🔔 **Arrival chime** — a soft two-tone ding for each new aircraft.
- ♪ **Ambient audio** — a quiet background drone.

Browsers only allow sound after you've tapped the page once.

## This session
Peak traffic (and when), highest and fastest aircraft seen, countries and
unique callsigns since you opened the page.

## Kiosk mode (wall display)
Add `?kiosk` to the address, e.g. `http://192.168.1.42/?kiosk`. Menus and
buttons are hidden, text is larger, and a highlight moves down the list
every 4 seconds. Ideal for an old tablet on the wall.

## Settings and About
See [Settings reference](settings.md). **About** describes the project and
data sources.
