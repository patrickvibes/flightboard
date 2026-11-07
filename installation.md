---
title: Install with the Arduino IDE
nav_order: 3
---

# Install with the Arduino IDE (advanced)

> **Most people should use [Install from your browser](install.md)** — it's
> one click and needs no software. This page is for building the firmware
> yourself, e.g. if you want to change the code.

This puts the Flight Board firmware on your ESP32 using the free Arduino IDE.
It takes about 20 minutes the first time, most of it downloads.

## 1. Install the Arduino IDE
Download it from [arduino.cc/en/software](https://www.arduino.cc/en/software)
and install it.

## 2. Add ESP32 support
1. Open **Settings / Preferences**.
2. In **Additional boards manager URLs**, add exactly one line:
   ```
   https://espressif.github.io/arduino-esp32/package_esp32_index.json
   ```
   Don't list it twice — duplicate URLs make the install fail.
3. Open **Tools → Board → Boards Manager**, search **esp32** (by Espressif
   Systems) and click **Install**. If it fails, remove it, restart the IDE and
   install once more.

## 3. Install the libraries
**Tools → Manage Libraries**, then install:
- **Adafruit SSD1306** (accept the prompt to install Adafruit GFX too)
- **ArduinoJson** by Benoit Blanchon — version 7 (tested with 7.4.3)
- **WiFiManager** by tzapu (tested with 2.0.17)

## 4. Open the sketch
Download the project folder (on GitHub: **Code → Download ZIP**) and unzip it.
The folder must be called `esp32_flight_tracker`, matching
`esp32_flight_tracker.ino` inside it. Open that `.ino` in the Arduino IDE;
the other code files open automatically as tabs.

## 5. Board settings
In the **Tools** menu set:

| Setting | Value |
|---|---|
| Board | **ESP32 Dev Module** |
| Partition Scheme | **Huge APP (3MB No OTA/1MB SPIFFS)** |
| Upload Speed | **115200** |
| Port | your board (see below) |

> The partition scheme will change when over-the-air updates arrive.

## 6. Connect and upload
1. Plug the board **directly** into your computer with a **data** cable.
   Avoid USB hubs — some won't detect the board.
2. Choose the new port under **Tools → Port** (on a Mac it looks like
   `/dev/cu.usbserial-…` or `/dev/cu.wchusbserial-…`).
3. Click **Upload** (→). When it says *Done uploading*, the board restarts and
   shows its boot animation.

If the port never appears or the upload fails, see
[Troubleshooting](troubleshooting.md#flashing).

## Next
[First-time setup →](first-setup.md)
