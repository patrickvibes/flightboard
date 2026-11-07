---
title: Hardware
nav_order: 2
---

# Hardware

## What you need
| Part | Notes | Approx. cost |
|---|---|---|
| **Ideaspark ESP32-WROOM-32 with built-in 0.96" OLED** | The reference board. Any ESP32 + SSD1306 128×64 OLED works if wired the same way (see below). | €8–12 |
| **USB data cable** | Must be a *data* cable, not charge-only. Micro-USB or USB-C to match your board. | €3 |
| **Piezo buzzer** *(optional)* | Passive piezo for beeps. | €1 |
| **USB power supply** | Any 5 V phone charger, once it's set up. | — |

The board needs **at least 4 MB of flash** (standard on ESP32-WROOM-32).

## Wiring
The reference board has the screen, button and LED built in — no wiring
needed except the optional buzzer.

| Function | ESP32 pin | Notes |
|---|---|---|
| OLED SDA | GPIO 21 | I²C, address `0x3C`, 128×64 SSD1306 |
| OLED SCL | GPIO 22 | |
| Button | GPIO 0 | The on-board **BOOT** button |
| Status LED | GPIO 2 | The on-board blue LED |
| Buzzer | GPIO 13 → buzzer → GND | Optional |

## Other boards
- **Other ESP32 boards with an OLED** (e.g. Heltec, TTGO) often use different
  pins and an OLED reset pin. These aren't configurable yet — support for
  board profiles is planned.
- **1.3" OLEDs** usually use an SH1106 controller, which isn't supported yet.
- **ESP32-S2 / S3 / C3** need a separate build and aren't supported yet.
