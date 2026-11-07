# Changelog

What's new in each Flight Board firmware release. Newest first.

<!-- Maintainers: versions are major.minor.patch. A release needs a
     "## [x.y.z] - YYYY-MM-DD" section; its first ~400 characters are shown on
     boards' dashboards, so keep the opening lines short and user-facing. -->

## [Unreleased]

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
