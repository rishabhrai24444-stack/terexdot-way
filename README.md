# Terexdot Way — Earth Intelligence

An interactive Earth exploration website and early-stage digital atlas. The project is intentionally transparent about what is measured, where data comes from, and which views are illustrative.

## Run locally
No build step is required. Open `index.html` through a local web server (recommended because browser modules/APIs and geolocation work more reliably):
- Python: `python -m http.server 8000`
- Then visit `http://localhost:8000`

GitHub Pages: Settings → Pages → Deploy from branch → `main` → `/ (root)`.

## Current modules
- Overview dashboard and animated 3D globe (Globe.gl)
- 3D Earth explorer with city markers, rotation, zoom, reset and atmosphere controls
- World Bank economy indicator explorer with historical chart
- Country profiles (population, GDP, GDP per capita, life expectancy)
- Open-Meteo current weather and 7-day forecast for selected locations
- NASA GIBS satellite browse imagery (daily true-colour layer)
- Biodiversity, forest and ocean discovery links

## Data sources
- World Bank Indicators API v2: https://datahelpdesk.worldbank.org/knowledgebase/articles/889392
- NASA GIBS: https://nasa-gibs.github.io/gibs-api-docs/
- Open-Meteo: https://open-meteo.com/en/docs
- GBIF: https://www.gbif.org/
- Global Forest Watch: https://www.globalforestwatch.org/
- NOAA: https://www.noaa.gov/

## Important data notes
- World Bank observations are annual and can be delayed. “Latest” means latest non-empty observation returned by the API, not a real-time value.
- Global population and GDP cards sum each country's latest non-empty observation. Because countries may report different years, these are indicative aggregates and should not be treated as an official same-year global total.
- City markers are illustrative reference points, not live location tracking.
- Weather is a forecast/model product from Open-Meteo, not a network of local sensors.
- NASA GIBS provides satellite browse imagery. It is not a live video feed; product dates and coverage vary.
- The ecosystem section currently provides curated discovery portals, not a measured real-time biodiversity dashboard.

## Stack
HTML, CSS, vanilla JavaScript, Globe.gl, TopoJSON client, World Bank API, Open-Meteo API and NASA GIBS WMS.

## Next engineering milestones
1. Add backend caching and scheduled ingestion for high-traffic deployments.
2. Add country boundary choropleths and robust ISO mapping.
3. Integrate vetted ocean, land-cover, emissions and biodiversity datasets with clear update timestamps.
4. Add user-created dashboards, saved places and comparison workspaces.
5. Add an AI research layer with source citations only after a secure server-side API integration.

## Attribution
Globe.gl: https://globe.gl/
World Bank data: https://data.worldbank.org/
NASA GIBS imagery acknowledgement: “We acknowledge the use of imagery provided by services from NASA's Global Imagery Browse Services (GIBS), part of NASA's Earth Science Data and Information System (ESDIS).”
