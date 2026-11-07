---
title: OpenSky account & usage limits
nav_order: 9
---

# OpenSky account & usage limits

Flight Board gets its data from the [OpenSky Network](https://opensky-network.org).
OpenSky limits how many requests each user can make per day, counted in
**credits**. Each update of your area costs one credit.

| Access | Credits per day |
|---|---|
| Anonymous (no account) | ~400 |
| Free OpenSky account | ~4,000 |

## How long will my credits last? (pacing)
Credits reset every day at **00:00 UTC** (midnight in Ireland in winter, 1 am in summer). With
**pacing** on (the default), the board does the maths for you: after each
update it divides the credits it has left by the time until the reset, and
slows down just enough that they last — so it **never runs dry mid-day**.
It never goes faster than your **Poll every** setting.

| Access | Credits per day | What pacing does at the default 60 s |
|---|---|---|
| Anonymous | ~400 | Settles at about **every 3–4 minutes**, all day |
| Free account | ~4,000 | Usually no change — 60 s fits comfortably |

When the board is pacing, the dashboard says **every 216s (paced)** and the
board's usage screen (double-tap) says **PACED 216S** instead of
**EVERY 60S**. Bigger scan areas (over 5° across) cost more credits per
update, and pacing allows for that too.

You can turn pacing off in **Settings → Display**. Without it, at 60 s an
anonymous board uses its ~400 credits in about 7 hours, then waits for the
reset.

**In short: get a free account** if you want frequent updates all day.

## Adding your account
1. Create a free account at [opensky-network.org](https://opensky-network.org).
2. In your account page, create an **API client**. OpenSky gives you a
   `credentials.json` file containing a `clientId` and `clientSecret`.
3. On the Flight Board dashboard, open **Settings → OpenSky account**.
4. Choose the `credentials.json` file and press **Load**.
5. The status changes to **Authenticated as …**.

The credentials are stored on the board only. The secret is never shown
again on the page. To go back to anonymous, press **Remove credentials**.

> **Keep `credentials.json` private.** Don't post it or share it. If it's
> ever exposed, delete that API client on OpenSky and create a new one.

## Checking your usage
- Dashboard: **Settings → Usage** shows credits left and roughly how long
  they'll last.
- Device: **double-tap** the button.
