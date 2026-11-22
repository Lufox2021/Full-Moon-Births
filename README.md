# Full Moon Births

An interactive data explorer for a college chemistry discussion exercise. Students commit to a
hypothesis about whether more babies are born at the full moon, lock it in, and are then given the
data and the tools to test it — without being told what to do with them.

**Live tool:** open `index.html`, or serve the folder over HTTP (the page fetches `births_moon.csv`).

## The data

`births_moon.csv` — 9,131 rows, one per calendar day, 1 January 1994 to 31 December 2014, United States.

| Column | Meaning |
| --- | --- |
| `date`, `year`, `month`, `day_of_month`, `day_of_week` | The calendar day |
| `births` | Number of births recorded in the United States that day |
| `source` | `CDC` or `SSA` — the two record series, which differ in level |
| `moon_phase` | One of eight named phases |
| `moon_age_days` | Days since the previous new moon |
| `moon_illuminated_pct` | Percent of the lunar disc lit |
| `holiday` | US federal holiday, if any |

Births from CDC natality files and Social Security Administration records. Lunar phase computed from
Meeus, *Astronomical Algorithms*, chapter 49.

## What the tool does

Hypothesis lock-in, filters, a sortable table, a plotting engine (response vs. a variable,
distributions, main effects, interactions) with least-squares fitting, summary statistics, and a
calculator for derived columns. State is kept in the browser.

## What students find

Births regressed on percent illuminated: slope **0.25 ± 0.64 births per percent**, R² = 0.000.
Spread across the eight lunar phases is 0.46% of the mean. Spread across days of the week is **46%**.
The data contains an enormous real effect, just not the one most students predict.
