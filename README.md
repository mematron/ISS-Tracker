# ISS-Tracker
Real-time ISS tracker. Processing (Java). Live telemetry via Where the ISS At? API. Windows.

# Orbital
### Real-Time ISS Tracker

Orbital is a live International Space Station tracker built in Processing (Java). It pulls telemetry from the [Where the ISS At?](https://wheretheiss.at) API and renders the station's current position over a hand-drawn contour map of Earth — updated every 10 seconds.

> Windows only. Closed source. Binary available in Releases.

---

## What It Shows

- **Position** — latitude and longitude plotted live on the map
- **Altitude** — current orbital height in kilometers (typically ~420–430 km, low Earth orbit)
- **Velocity** — current speed in km/h
- **Visibility** — whether the ISS is in daylight, eclipse (shadow), or the terminator zone

All telemetry displayed in the upper left, refreshed every 10 seconds.

---

## Design

The visuals are intentional. No clutter, no photorealism — everything is drawn in values of gray against a dark field.

- **Earth map** — hand-traced contour drawing of the continents and major oceans. Started from a flattened projection, simplified down to clean outlines.
- **ISS icon** — a custom silhouette illustration of the station. Scalable with `+` / `−` keys.
- **Target reticle** — a circle around the ISS icon so your eye lands on it immediately.
- **Window** — fully resizable. The map and station scale with it.

The aesthetic was inspired by real and imaginary interfaces — the kind of display you'd expect to see in a facility that actually tracks things.

---

## Technical

- **Language:** Processing (Java)
- **API:** [Where the ISS At?](https://wheretheiss.at) — `https://api.wheretheiss.at/v1/satellites/25544` — returns latitude, longitude, altitude, velocity, visibility
- **Update rate:** Every 10 seconds (API updates every 5s; 10s is sufficient and less aggressive)
- **Frame rate:** 60fps continuous redraw — the window title updates with station data on every frame
- **Codebase:** ~239 lines
- **Platform:** Windows 10 or later

---

## Demo

[![Orbital Demo 1](https://img.youtube.com/vi/lVaSiyoWAwA/0.jpg)](https://www.youtube.com/watch?v=lVaSiyoWAwA&t=122s)
[![Orbital Demo 2](https://img.youtube.com/vi/JzaEnWLwKNg/0.jpg)](https://www.youtube.com/watch?v=JzaEnWLwKNg&t=156s)

---

## Download

See [Releases](../../releases) for the Windows binary.

---

## Part of the mematron ecosystem

[ardorlyceum.itch.io](https://ardorlyceum.itch.io) · [linktr.ee/mematron](https://linktr.ee/mematron)

