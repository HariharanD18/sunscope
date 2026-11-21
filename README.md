# ☀️ SunScope – Live Solar Planner

A real-time web app that uses live weather data to estimate solar panel output and recommends the **best time to run household appliances** so they run on free solar energy, reducing electricity bills and carbon emissions.

## Features
- Live sunlight, temperature and cloud cover for any location (auto-refreshes every 10 minutes)
- Solar power estimate for right now, today and tomorrow (kWh)
- 24-hour power forecast bar chart (drawn with Canvas, no libraries)
- Appliance scheduler: finds the start time with the highest solar coverage
- CO₂ savings estimate
- Single HTML file, no backend, no installation

## How it works
1. Gets your location (GPS or manual latitude/longitude).
2. Fetches hourly sunlight and temperature from the free [Open-Meteo API](https://open-meteo.com/).
3. Estimates output per hour:
   `Power = panel kW × (sunlight ÷ 1000) × 0.75 × heat correction`
4. For each appliance, tests every start time in the next 24 hours and picks the one where solar output covers the most of its power need.

## Run it
Open `index.html` in any modern browser (internet needed for live data).

## Tech stack
HTML · CSS · JavaScript · Canvas · Open-Meteo API

## Limitations
- Output is an estimate, assuming a flat 75% system efficiency.
- Does not yet consider panel tilt, shading or battery storage.

## Roadmap
- Electricity bill savings in ₹
- Battery storage simulator
- Panel tilt and orientation settings
- "Run it now" notifications

## License
MIT
