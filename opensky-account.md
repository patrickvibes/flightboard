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

## How long will my credits last?
| Poll every | Requests per day | Anonymous (~400) | Account (~4,000) |
|---|---|---|---|
| 30 s | 2,880 | ~3 h | ~33 h ✅ |
| 60 s *(default)* | 1,440 | ~7 h | ✅ all day |
| 120 s | 720 | ~13 h | ✅ all day |
| 240 s* | 360 | ✅ all day | ✅ all day |

\*The Settings page currently allows up to 120 s.

**In short: get a free account** if you want the board running all day. When
credits run out, the board backs off and waits until OpenSky allows requests
again; the dashboard shows a rate-limit notice.

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
