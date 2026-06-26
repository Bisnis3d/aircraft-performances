# lnmperf-profiles

Aircraft performance profiles (`.lnmperf`) for [Little Navmap](https://albar965.github.io/littlenavmap.html), covering the GA aircraft in my MSFS 2024 hangar.

All profiles are based on the official aircraft manuals or MSFS simulation data, cross-referenced field by field. Values are chosen for planning realism — not maximum book performance, but conservative and internally consistent numbers you can actually trust for fuel and TOC/TOD calculations.

## Profiles

| File | Aircraft | Cruise ref | Cruise speed | Fuel flow |
|---|---|---|---|---|
| `Cessna_414AW.lnmperf` | Cessna 414AW RAM Series IV | 10,000 ft / 65.5% BHP ISA | 188 kt TAS | 39 gph |
| `Milviz_Cessna_310R.lnmperf` | Milviz Cessna 310R | 8,500 ft / lean mixture | 185 kt TAS | 34 gph |
| `A2A_Piper_Aerostar_PA-60-600.lnmperf` | A2A Piper Aerostar 600 | 7,500 ft / 67% best economy | 210 kt TAS | 28 gph |
| `A2A_Piper_Pa-24-250_Comanche.lnmperf` | A2A Piper PA-24-250 Comanche | 75% power leaned | 150 kt TAS | 14 gph |

## Installation

Copy the `.lnmperf` files to your Little Navmap aircraft performance folder:

- **Windows**: `%APPDATA%\ABarthel\Little Navmap\aircraft_perf\`
- **macOS / Linux**: `~/.config/ABarthel/Little Navmap/aircraft_perf/`

Then load a profile via `Aircraft → Load Aircraft Performance…` or set it as default in `Aircraft → Edit Aircraft Performance…`.

## Key design choices

Every profile follows these rules:

- **RunwayType: HARD** — all four aircraft are retractables; soft field ops are non-standard.
- **Descent speed < Cruise speed** — avoids LNM placing TOD unrealistically close to destination.
- **Alternate speed and fuel flow < Cruise** — alternate legs are flown at lower altitude and reduced power, so alternate FF matching cruise FF overstates fuel burn.
- **Contingency: 5%** — ICAO standard for all profiles.
- **Climb VS** sourced from manual (max or cruise climb), applied conservatively for en-route planning.

## Notes

- Fuel units are **gallons** (volume mode, Avgas).
- All speeds are **TAS**, as required by Little Navmap.
- The C414 profile is based on the RAM Series IV MSFS simulation data table, not the stock Cessna 414 POH.
- Profiles are tuned for MSFS 2024 but will work in any LNM installation regardless of simulator.

## License

MIT
