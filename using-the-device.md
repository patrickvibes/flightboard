---
title: Using the device
nav_order: 5
---

# Using the device

## The screen
The OLED shows one aircraft at a time:

```
03/12              SHANNON   ← which flight of how many (* = locked) · your area
──────────────────────────
EIN105                       ← callsign
AER LINGUS SNN>JFK           ← airline and route (or country, if unknown)
18.2KM AWAY             ~4M  ← distance · minutes to its closest approach
36000FT ▲            845KMH  ← altitude (▲ climbing, ▼ descending) · speed
▬▬▬▬▬▬▬▬▬▬▬▬                 ← Ticker mode: time left before the next flight
```

A small **↑** in the top-right corner means a firmware update is available
(see [Update your board](update.md)).

With no aircraft in range you'll see **Quiet sky**: a radar sweep that turns
once per update, your area, the scan size and when the next scan is due.

Flights are ordered nearest first. Two display modes (set in
[Settings](settings.md)):
- **Step** — stays on a flight until you tap the button.
- **Ticker** — moves to the next flight automatically every few seconds.
  The callsign row scrolls with the airline and route, and a bar along the
  bottom shows the time left before the next flight.

If you **lock** a flight from the web dashboard, the screen stays on it
until you unlock it.

## Overhead moment
When a plane comes within **3 km** of you (measured along the ground, at any
height), the board marks the moment:

- a rising **four-note chime** and four LED blinks,
- the screen **flashes** for a few seconds, then shows **OVERHEAD NOW** with
  the callsign, live distance and altitude, and a 10-block meter that fills
  as the plane gets closer (full inside 1.2 km),
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
| **Tap** | Next flight. On any other screen (usage, address, alerts, overhead, no data): back to the flights. |
| **Double-tap** | **API usage** for 5 seconds: credits left and roughly how long they'll last, requests so far, how often it updates (**PACED** when it's slowed down to make credits last the day). |
| **Hold ~1 s**, then let go | **Address** for 15 seconds: the board's IP and a **QR code** — scan it with your phone camera to open the dashboard. |
| **Keep holding** (past ~2 s) | **Reset Wi-Fi** countdown: a bar fills to 5 seconds. **Let go to cancel.** At 5 seconds it forgets Wi-Fi and opens the setup hotspot — you don't need to let go. |

Screens that time out (usage, address, alerts) show a thin bar along the
bottom that shrinks until they close.

## Alert screens
These take over the screen for a few seconds, then it goes back to the
flights (tap to go back sooner):

- **Close approach** — a flight will pass within your alert distance (set in
  [Settings](settings.md)). Shows how close it will pass, where it is now and
  a track marker moving toward its closest point. With three LED blinks and
  a beep.
- **Emergency squawk** — an aircraft in range is squawking 7500, 7600 or
  7700. The whole screen turns white with the code, what it means, where the
  aircraft is (distance and direction) and whether it's climbing or
  descending. The LED strobes.
- **Update available** — once per new version: open the dashboard for how
  to update.

## When there's no data
If OpenSky stops answering — rate limited, an error, or Wi-Fi drops — the
screen says so: **THROTTLED**, **API ERROR** or **OFFLINE**, why, how often
it's retrying and when the next try is. The flights from the last good
update are kept; tap to look at them. It goes back to normal by itself on
the next good update.

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
