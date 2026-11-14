# Trainuck timetables

The rail timetables the Trainuck app downloads for its cities other than Edmonton, rebuilt every Sunday
from each city's GTFS feed by a GitHub Action in the Trainuck project. Please don't edit these files
by hand: the next run replaces them.

- `index.json`: each city's build time, the dates it covers, its trips and size. The app reads this
  first and downloads only the cities newer than the ones on the phone.
- `cities/<city>.json`: a city's timetable, in the format of Edmonton LRT Live's `lrt.json`.
- `feeds-seen.json`: the ETag, date and size of each feed every city was last built from.

| City | Dates | Trips | Built |
|---|---|---|---|
| Calgary | 2026-10-13 – 2026-12-20 | 2,629 | 2026-11-14 |
| Montréal | 2026-08-24 – 2027-01-03 | 16,742 | 2026-11-08 |
| Ottawa | 2026-11-13 – 2026-12-13 | 2,353 | 2026-11-14 |
| Toronto | 2026-11-04 – 2026-11-27 | 17,212 | 2026-11-05 |
| Metro Vancouver | 2026-09-07 – 2027-01-03 | 5,409 | 2026-11-14 |
| Waterloo Region | 2026-07-05 – 2028-07-03 | 473 | 2026-11-04 |

## Data and licences

The timetables are derived from open data:

| City | Feed | Licence |
|---|---|---|
| Calgary | Calgary Transit, data.calgary.ca (npk7-z3bj) | Open Government Licence – City of Calgary |
| Ottawa | OC Transpo GTFS | OC Transpo open data terms |
| Waterloo Region | GRT ION light rail feed | Region of Waterloo open data licence |
| Toronto | TTC, GO Transit and UP Express (Metrolinx), VIA Rail | City of Toronto Open Data Licence, Metrolinx open data terms, VIA Rail open data terms |
| Vancouver | TransLink | TransLink open data terms |
| Montréal | STM, REM, exo (trains) | STM open data terms, REM open data terms, CC BY 4.0 (exo) |

Trainuck is a personal project, not made by or connected with any of these agencies. For service
changes and alerts, check the agency.
