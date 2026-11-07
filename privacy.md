---
title: Privacy & data
nav_order: 12
---

# Privacy & data

## What the board stores
On the board's own flash memory only:
- your Wi-Fi network name and password,
- your location (coordinates and place name) and other settings,
- your OpenSky credentials, if you add them.

None of this is sent to the Flight Board project. The only contact with the
project's website is the optional update check, which sends no ID or
settings. There is no account, analytics or tracking.

## Who the board talks to
| Service | Why | What it sends |
|---|---|---|
| [OpenSky Network](https://opensky-network.org) | Live aircraft positions; aircraft details | The edges of your scan area; your OpenSky credentials if added; an aircraft's ID when you open its details |
| [OpenStreetMap Nominatim](https://nominatim.org) (place search) | Turning a place name into coordinates | The place name you type |
| [adsbdb.com](https://www.adsbdb.com) | Flight routes | A flight's callsign, when you open its details |
| Flight Board website (GitHub Pages) | Checking for a newer firmware version, twice a day (can be turned off) | Nothing but the request itself — no ID or settings |

## What your browser loads
- The dashboard page itself comes from the board.
- The page loads the [Leaflet](https://leafletjs.com) map library from
  unpkg.com, map tiles from [OpenStreetMap](https://www.openstreetmap.org),
  and its display font from Google Fonts. These services see your IP address, as with any
  web page.
- Sound and traffic-history preferences are saved in your browser.

## Your location
Your scan area is sent to OpenSky with every update — that's how it knows
which aircraft to return. Use a nearby town rather than your exact address
if you prefer.

## Security notes
- The dashboard has no password. Anyone on your Wi-Fi can open it and change
  settings. Don't put the board on a network you don't trust, and never
  expose it directly to the internet.
- The board doesn't verify the security certificates of the services it
  contacts. That's acceptable for public flight data, but it's one reason
  the board should only hold credentials that are low-risk (like an OpenSky
  API client) and easy to replace.
