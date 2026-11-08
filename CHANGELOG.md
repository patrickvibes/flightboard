# Changelog

What's new in each Flight Board firmware release. Newest first.

<!-- Maintainers: versions are major.minor.patch. A release needs a
     "## [x.y.z] - YYYY-MM-DD" section; its first ~400 characters are shown on
     boards' dashboards, so keep the opening lines short and user-facing. -->

## [Unreleased]

## [1.3.1] - 2026-11-08
Check for updates whenever you like.

- Settings → Firmware has a **Check now** button: see straight away
  whether a newer version is out, instead of waiting for the twice-daily
  check.
- Website: the radar on the home page now sweeps and pings.

## [1.3.0] - 2026-11-08
A clearer live map, and a new website.

- Live map: aircraft arrows now point the way the plane is actually
  heading (they were a quarter-turn off).
- Live map: aircraft and their trails are coloured by altitude, and trails
  fade from where the plane entered your area to solid at its position.
- "Use my current location" now explains why phones won't share location
  with the board's page, instead of a bare "Permission denied".
- New website, with a guide to how the coming game mode will score.
  Every old link still works; the docs overview is now at /docs/.

## [1.2.0] - 2026-11-07
Your OpenSky credits now last all day.

- Credits now last all day: the board paces its updates so OpenSky's daily
  allowance runs until the midnight (UTC) reset instead of running out in
  the afternoon. Without an account it updates every few minutes, all day.
  Can be turned off in Settings.

## [1.1.0] - 2026-11-07
New look for the board's screen.

- New screens on the board: a cleaner flight view with airline and route
  codes, a radar "quiet sky" when nothing's around, close-approach and
  emergency alert screens, and a "no data" screen that says why and when
  it'll retry.
- Hold the button for 1 s to get a QR code that opens the dashboard.
- Wi-Fi reset now shows a countdown bar: let go to cancel; it fires at 5 s.
- Overhead screen redesigned with a closeness meter.

## [1.0.0] - 2026-11-07
First versioned release.

- Overhead moment on the board: a chime, a screen flash and an OVERHEAD NOW
  screen when a plane passes within 3 km, with a live countdown.
- Soft tick while a plane is overhead (can be turned off in Settings).
- The board now tells you when a new version is out (Settings → Firmware).
- Install and update from your browser, no Arduino IDE needed.
- Cleaner traffic chart: the label no longer overlaps the line.
