---
title: Install from your browser
nav_order: 2.5
---

# Install from your browser

The quickest way to put Flight Board on your board. No Arduino IDE, no
downloads — just Chrome or Edge on a computer.

<script type="module" src="https://unpkg.com/esp-web-tools@10.4.0/dist/web/install-button.js?module"></script>

<esp-web-install-button manifest="{{ site.baseurl }}/firmware/manifest.json">
  <span slot="unsupported">Your browser can't do this. Please use <b>Chrome</b> or <b>Edge</b> on a
  computer (not a phone or Safari/Firefox).</span>
  <span slot="not-allowed">This page must be opened over HTTPS.</span>
</esp-web-install-button>

## Steps
1. Plug the board **directly** into your computer with a USB **data** cable
   (not a hub — and not a charge-only cable).
2. Click **Connect** above and choose the port that appears when you plug the
   board in (it may be called "USB Serial" or `cu.usbserial-…`).
3. Click **Install Flight Board**.
   - **First install on this board:** tick **Erase device**.
   - **Updating:** leave **Erase device unticked** — your Wi-Fi, location and
     settings are kept.
4. Wait for it to finish (2–3 minutes), then close the dialog.
5. Unplug and replug the board (or press its **EN / RST** button). You'll see
   the boot animation.

New board? Carry on with [First-time setup](first-setup.md).

## If it doesn't connect
- Try another USB cable — many are charge-only.
- Hold the board's **BOOT** button while you click **Connect**, then let go.
- On Windows you may need the **CH340** USB driver from the board maker.
- Still stuck? Use the [Arduino IDE method](installation.md) instead.

## What gets installed
The latest release — see [what's new](whats-new.md). The firmware files are
published in the [Flight Board repository](https://github.com/patrickvibes/flightboard).
