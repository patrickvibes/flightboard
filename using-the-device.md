---
title: Using the device
nav_order: 5
---

# Using the device

## The screen
The OLED shows one aircraft at a time:

```
3/12* ~4m Shannon        ← position in list, * = locked, minutes to closest approach, your area
EIN123  Aer Lingus  DUB->JFK   ← big line, scrolls if too long
14.2 km away
11000 ft  780 kmh
```

- **Top line:** which flight of how many, a `*` if it's locked, minutes until
  its closest approach (if it's coming towards you), and your area name.
- **Big line:** the callsign, plus the airline and route when known
  (otherwise the country it's registered in). It scrolls when it doesn't fit.
- **Bottom lines:** distance from you, altitude and speed.

With no aircraft in range it shows **No flights … watching…**.

Flights are ordered nearest first. Two display modes (set in
[Settings](settings.md)):
- **Step** — stays on a flight until you tap the button.
- **Ticker** — moves to the next flight automatically every few seconds.

If you **lock** a flight from the web dashboard, the screen stays on it
until you unlock it.

## Overhead moment
When a plane comes within **3 km** of you (measured along the ground, at any
height), the board marks the moment:

- a rising **four-note chime** and four LED blinks,
- the screen **flashes** for a few seconds, then shows **OVERHEAD NOW** with
  the callsign, airline, live distance, altitude, speed and heading,
- the screen is **brightest when the plane is closest** and dims as it moves
  away toward the edge of the zone,
- a **soft tick** every 5 seconds while it's still overhead (can be turned
  off in [Settings](settings.md)),
- the blue LED stays **on** until the plane leaves.

The board checks OpenSky about once a minute, but planes cross the zone in
under 30 seconds. So between updates it **estimates** where each plane is
from its speed and heading, twice a second. The distance shown is that live
estimate.

**Tap the button** to dismiss the overhead screen for that plane. It also
takes priority over a flight you've locked; the locked flight comes back when
the plane leaves. If the same plane drifts out and back in within 2 minutes,
it doesn't chime again.

## The button (BOOT)
| Action | What it does |
|---|---|
| **Tap** | Next flight (on the overhead screen: dismiss it) |
| **Double-tap** | Show OpenSky usage for 5 seconds: anonymous/authenticated, credits left, requests this session, current interval (and **THROTTLED** if rate-limited) |
| **Hold ~1 s** | Show the board's web address |
| **Hold ~5 s**, then release | Forget Wi-Fi and reopen the setup hotspot |

When you've held long enough for a Wi-Fi reset, the screen says
**Release to reset Wi-Fi**. Let go before then to cancel.

## The blue LED
| Pattern | Meaning |
|---|---|
| 2 quick blinks | A new aircraft has entered your area |
| 3 medium blinks | An aircraft will pass within your alert distance |
| Fast strobe (~2 s) | An aircraft is squawking an emergency code (7500 / 7600 / 7700) |
| 4 blinks, then steady on | A plane is overhead (stays on until it leaves) |
| Slow steady blink | Problem with Wi-Fi or OpenSky |

The LED can be turned off in Settings.

## The buzzer (optional)
If you've fitted a piezo buzzer:
- **ding-dong** — new arrival,
- **single high beep** — close approach (if an alert distance is set),
- **double two-tone** — emergency code,
- **rising four-note chime** — a plane is overhead, then a **soft tick**
  every 5 seconds while it stays overhead.

Turn it off with **Mute beep** in Settings.
