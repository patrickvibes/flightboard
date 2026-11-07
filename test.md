---
title: Test builds
nav_exclude: true
search_exclude: true
---

# Test builds

**Work-in-progress firmware for testing.** It may have bugs. For normal use,
install from [Install from your browser](install.md) instead.

<p id="testinfo">Loading build details…</p>

<script type="module" src="https://unpkg.com/esp-web-tools@10.4.0/dist/web/install-button.js?module"></script>

<esp-web-install-button manifest="{{ site.baseurl }}/firmware/test/manifest.json">
  <span slot="unsupported">Use <b>Chrome</b> or <b>Edge</b> on a computer.</span>
  <span slot="not-allowed">This page must be opened over HTTPS.</span>
</esp-web-install-button>

## Steps
1. Plug the board in with a USB data cable, directly (no hub).
2. Click **Connect** and choose the board's port.
3. Click **Install**. Leave **Erase device unticked** to keep your Wi-Fi and
   settings (tick it only if the board is misbehaving and you want a clean
   start).
4. When it finishes, unplug and replug the board.

Test builds show **TEST-…** on the boot screen and don't show update
notices. To go back to the normal version, install from
[Install from your browser](install.md).

<script>
fetch("{{ site.baseurl }}/firmware/test/info.json", {cache: "no-store"})
  .then(r => r.ok ? r.json() : Promise.reject())
  .then(i => {
    const el = document.getElementById("testinfo");
    el.textContent = "Build " + i.version + " · branch " + i.branch + " · " + i.built;
  })
  .catch(() => { document.getElementById("testinfo").textContent = "No test build published yet."; });
</script>
