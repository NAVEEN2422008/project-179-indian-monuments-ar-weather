# c179 - Indian Monuments Navigation + AR Weather

A two-page map app: the first page shows a Mapbox map with markers for famous Indian monuments (Amber Fort, Gateway of India, India Gate, Lotus Temple, Victoria Memorial) and a destination geocoder; the second page receives the selected coordinates via URL query string.

## Features
- Browser geolocation to center the map on the user.
- Mapbox GL map with custom image markers for 5 Indian monuments.
- Mapbox Geocoder to search a destination.
- Navigate button passes `source`/`destination` lat/lon coordinates to `ar_weather.html` via query string.
- `ar_weather.js` parses those coordinates from the URL.

## Tech Stack
- Mapbox GL JS 2.1.1 + Mapbox Geocoder
- jQuery, Bootstrap 4

## Project Structure
```
c178/
├── main.html        # map page with monument markers
├── main.js          # geolocation + mapbox init + marker placement
├── ar_weather.html  # destination page (reads query params)
├── ar_weather.js    # parses source/destination coordinates
├── main.css
└── assets/          # monument marker images
```

## Installation
No build step; CDN-based. Requires a Mapbox access token (embedded in `main.js`).

## Usage
Serve the folder statically and open `main.html` in a browser. Allow location access, choose a destination, then press the navigate button.