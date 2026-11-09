# Gatun Lake Transit Capacity Monitor

### 👉 [Open the live dashboard](https://gatun-lake-live-monitor.pages.dev)

A live dashboard that tracks and forecasts Gatun Lake's water level,
the constraint that limits how many ships transit the Panama Canal
each day and how deeply they can be loaded.

## What it does

- **Live**: the lake level from the Panama Canal Authority's gauge,
  updated every 15 minutes, mapped onto six capacity zones
  (ships per day and maximum draft).
- **Seasonal**: compares this year with the last five years
  for the same date.
- **Forecast (new)**: projects the lake up to 180 days ahead, with a
  likely range and the dates when draft restrictions could begin.

## How the forecast works

- A statistical model trained on daily lake data since 1965, using
  the current level, trend, season and El Niño
- Cross-checked against the ECMWF seasonal rainfall outlook and
  dry, typical and wet scenarios
- Reruns automatically every night

**Backtested on 2015–2026**, years the model never saw in training:
average miss of 0.6 ft at 30 days, 1.2 ft at 90 days and 1.8 ft at
180 days. The likely range captured 78–90% of actual outcomes.

## Limitations

The model learns how the lake behaves, not the canal authority's
decisions. In 2023–24 the lake held up despite El Niño because
transits were cut to conserve water. This is an experimental
estimate, not an official ACP outlook.

## Data sources

Panama Canal Authority (ACP) · NOAA CPC · ECMWF SEAS5 and ERA5
via Open-Meteo (CC BY 4.0)

---

Built by Jerald Seet Jin · [LinkedIn](https://www.linkedin.com/in/jerald-seet-45943b296)
