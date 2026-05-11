# Privacy Policy — Boating Navigation

**Last updated:** 11 May 2026
**Effective date:** 11 May 2026

This Privacy Policy explains how the **Boating Navigation** mobile application
("the app", "we", "us") handles your information. Read it carefully before
using the app.

The short version: **we do not run a server, we do not collect your data, we
do not create user accounts, and we do not track you across apps or websites.**
The app stores everything locally on your device. The only data that leaves
your device are the minimum requests needed to fetch a map tile, a weather
forecast, or a geocoding result, plus the ads SDK calls described below.

---

## 1. Information we do NOT collect

The app does not have a backend server. We never receive, see, store, or sell:

- Your name, email, phone number, or any account information
- Your GPS history, routes, trips, anchor positions, or vessel data
- Your boat profile (vessel name, MMSI, length, type)
- Your logbook entries
- Your search history inside the app
- Any analytics about how you use the app

There are no user accounts. You do not sign up. You do not log in.

## 2. Information stored locally on your device

The following are stored **only on your phone**, in the app's private storage
sandbox provided by iOS or Android:

- Live GPS position (used to render the vessel cursor on the chart)
- Course over ground (COG), speed over ground (SOG), heading
- Saved routes and waypoints you create
- Recorded passages / tracks
- Anchor alarm position and radius
- Man-Overboard (MOB) drop point and timestamp
- Boat profile fields you enter (vessel name, MMSI, length, type)
- App settings (units, map style, night mode, feature toggles)
- Offline map regions you choose to download
- Cached map tiles
- Cached ad configuration

Uninstalling the app deletes all of this data. We have no way to recover it.

## 3. Permissions the app requests, and why

| Permission | Why the app asks for it |
|---|---|
| **Location (When in Use)** | To show your vessel on the chart, compute course over ground (COG) and speed over ground (SOG), record passages, plan routes, and place a Man-Overboard drop point at the correct coordinates. |
| **Location (Always / Background)** | So tracking and the anchor alarm continue to work with the screen off during an overnight passage. The app shows a foreground service notification on Android whenever background location is active. |
| **Notifications** | So the anchor drag alert and the MOB banner can wake the helm even when the app is in the background. |
| **Vibration** | To deliver haptic feedback on alarms (anchor drag, MOB). |
| **Internet** | To download map tiles, weather forecasts, geocoding results, optional AIS ship data, ad config, and ads. |

You can revoke any of these permissions at any time from your device settings;
the affected features will stop working but the app will not crash.

## 4. Data that leaves your device (third-party services)

The following requests are sent to third-party services. Each request contains
only the minimum information needed to answer it.

### 4.1 Map tiles — OpenStreetMap & OpenSeaMap

- **What is sent:** Tile coordinates (z/x/y), a `User-Agent` string identifying
  the app version
- **Sent to:** `tile.openstreetmap.org`, `tiles.openseamap.org`
- **Why:** To render the marine chart and the seamark overlay
- **Their policies:** https://wiki.osmfoundation.org/wiki/Privacy_Policy

### 4.2 Weather — Open-Meteo

- **What is sent:** Coordinates (latitude, longitude) of the area you want the
  forecast for
- **Sent to:** `api.open-meteo.com`
- **Why:** To fetch the current weather and short-term forecast
- **Their policy:** https://open-meteo.com/en/terms

### 4.3 Geocoding — Nominatim (OpenStreetMap)

- **What is sent:** The text you type into the search bar, or coordinates for
  reverse geocoding, plus the `User-Agent` of the app
- **Sent to:** `nominatim.openstreetmap.org`
- **Why:** To resolve harbour names, ports, or place names into coordinates
- **Their policy:** https://operations.osmfoundation.org/policies/nominatim/

### 4.4 Bathymetry — Open Topo Data

- **What is sent:** Coordinates of the point you tap on the chart
- **Sent to:** `api.opentopodata.org`
- **Why:** To return the seafloor depth at the tapped point
- **Their policy:** https://www.opentopodata.org/

### 4.5 AIS ship tracking — AISStream.io (OPTIONAL, off by default)

- **Only used when you enable AIS in Settings AND provide your own API key.**
- **What is sent:** Your API key, a bounding box of the chart area you are
  viewing
- **Sent to:** `stream.aisstream.io`
- **Why:** To stream nearby commercial-ship positions in real time
- **Their policy:** https://aisstream.io/

### 4.6 Ads — Google AdMob

- **What is sent:** Standard Google Mobile Ads SDK requests, which include
  your device's advertising identifier (ADID on Android, IDFA on iOS, only if
  you have not disabled it in OS settings), basic device information, and the
  ad unit identifier
- **Sent to:** Google AdMob servers
- **Why:** To serve banner, native, interstitial, and rewarded ads. We do not
  receive personal data about you from Google.
- **Their policy:** https://policies.google.com/technologies/ads
- **Frequency:** Ads are gated by a frequency cap, are never shown during
  active tracking sessions, and are never shown on the live chart screen.
- **Opt-out:** Watching one rewarded ad grants a 24-hour ad-free window.

### 4.7 Ad configuration — GitHub Gist

- **What is sent:** Standard HTTPS GET request, no personal data, no
  identifiers
- **Sent to:** `gist.githubusercontent.com`
- **Why:** To fetch the latest ad unit identifiers and feature flags so we can
  disable a misbehaving ad placement without shipping a new app version

### 4.8 Feature flags — Firebase Remote Config

- **What is sent:** Standard Firebase Remote Config SDK request (anonymous
  device install token, app version, locale)
- **Sent to:** Google Firebase
- **Why:** To toggle non-critical feature flags remotely
- **Their policy:** https://firebase.google.com/support/privacy

## 5. SMS (Man-Overboard / distress)

When you trigger the MOB / SOS button, the app **opens your phone's default
SMS composer** pre-filled with the coordinates of the drop point and a short
distress message. The app does **NOT** send the SMS automatically — you must
tap "Send" in your messaging app. The SMS is sent from your device, by your
carrier, to the maritime authorities listed in the bundled `emergency_contacts.json`.

**Important:** This is NOT a satellite SOS service and is NOT a replacement for
VHF Channel 16 or a registered EPIRB. It requires cellular coverage to work.

## 6. Sharing data with third parties

We do not sell, rent, or share your personal data because we do not collect it.

You can manually share data with third parties through your own actions:

- **GPX export** — you can save a GPX file of a route or track and share it
  via any app you choose (e.g. AirDrop, email, WhatsApp). What you share is
  your choice.
- **SMS composer** — the MOB flow opens your SMS app pre-filled. You choose
  whether to send.

## 7. Children

The app is rated 4+ on the App Store and "Everyone" on Google Play. It does
not knowingly collect data from any user. The app contains general-audience
advertising via Google AdMob; per AdMob policy, no personalized ads are
served to users tagged as children.

## 8. Security

Local data is stored in the app's private sandbox provided by iOS or Android.
We do not transmit your personal data because we do not collect it. Map
tiles, weather, geocoding, and ad requests are sent over HTTPS / WSS.

## 9. International users

The app is available worldwide. Because we do not run servers and do not
collect personal data, the GDPR (EU), CCPA (California), and similar
regulations apply only to data collection by the third parties listed in
section 4. Refer to each third party's policy for their compliance posture.

## 10. Changes to this policy

If we change this Privacy Policy, the "Last updated" date at the top will
change and the new version will be published at the same URL the app links
to. Material changes will be highlighted at the top of this document.

## 11. Contact

For privacy questions about this app, contact:

**Email:** support@boatingnav.app

If you do not have an email, you can open an issue on the public repository at
`https://github.com/melianinadia391-blip` (or the equivalent address linked
from the app's About screen).

---

© 2026 Boating Navigation. Distributed under the app's License (see About
screen inside the app).
