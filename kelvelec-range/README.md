# Voqa x Kelvelec EV range calculator

Jointly branded calculator showing how many miles of range different AC and DC chargers add to an EV in a given dwell time.

## Status

**Draft, live but unlisted, awaiting Kelvelec sign-off.**

Published at `https://tools.voqa.com/kelvelec-range/` so Kelvelec can review it on a Voqa address. While in draft it:

- has `<meta name="robots" content="noindex, nofollow">` so search engines don't list it
- shows a "Draft for review · not yet published" label above the first heading
- is not linked from the tools.voqa.com homepage or the root `README.md`

The code is public on GitHub, so treat "unlisted" as low-profile, not private.

Last updated 18/11/2026.

## What's changed from `/ev-charging/` (v1.1.0 → v1.2.0)

- 27-car list from EV Database UK (November 2026), sorted A–Z, with per-model usable battery, efficiency, max AC and max DC
- Charger options 7.4, 11 and 22 kW (AC) and 50, 150 and 200 kW (DC)
- Dwell times from 10 minutes to 8 hours, including 10, 20, 30 and 45 minutes for DC
- Arrival state of charge selector (10–90%)
- Custom vehicle takes efficiency, battery, max AC and max DC
- Car-specific notes, e.g. when a car can't use the charger's full power, or uses CHAdeMO
- Joint header: Voqa logo left on teal, Kelvelec white logo right on Kelvelec olive, split by a gold diagonal at the midpoint
- Removed: header title and CTA, bottom booking CTA, privacy pop-up, "How to use" section, charging rate and efficiency tiles

## How the figures work

- **AC:** the car charges at the lower of the charger rating and its on-board charger limit, up to 100%.
- **DC:** charging stops at 80%. Speed follows a standard curve (full power to 50%, easing to half power by 80%), scaled per car so its 10–80% time matches EV Database UK and capped at the car's max DC rate.
- Figures are energy into the battery. Charging losses are not modelled.

## Before go-live

- [ ] Kelvelec sign-off on logo use, colours and wording
- [ ] Confirm Kelvelec olive and gold hex codes (currently `#545837` and `#CFB06F`, sampled from their emails)
- [ ] SVG logo from Kelvelec (current file is a PNG made from the white logo Olivia sent on 18/11/2026)
- [ ] Remove the draft label (`.draft-label` in `index.html`) and the `robots` noindex meta tag
- [ ] Add the tool to the table in the root `README.md` and, if wanted, the tools.voqa.com homepage

## Known approximations

- Cars with an optional 22 kW on-board charger (iX3, Countryman, EX30, Q6) use the standard 11 kW
- Škoda Enyaq 85 DC figures are taken from the Elroq 85 (same platform)
- Custom vehicles follow the standard curve straight from the entered peak, so they look slightly quicker than a listed car with the same peak

## Data

EV Database UK (ev-database.org/uk), pulled 18/11/2026. Per-car figures are in the `VEHICLES` object in `index.html`.
