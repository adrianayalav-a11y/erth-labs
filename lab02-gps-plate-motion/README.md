# Lab 2 — GPS Plate Motion

Python reproduction of ERTH 2001 Lab 2, originally completed as an Excel workbook of GPS position time series. The notebook walks through the lab step for step: north and east components at five California stations, a five-year rate in each direction, a horizontal speed from the Pythagorean theorem, velocity vectors, and a map of three neighboring stations along the San Andreas system. A short extra section at the end compares the lab's two-endpoint rate with a least-squares fit over the same window; that comparison is not part of the original lab.

The notebook explains the concept of each step: every code cell has a plain-language introduction before it and a short "what this shows" after it. It does not include answers to the lab's graded questions.

AI used: Python notebook built with help from an AI coding agent.

## Files

- `lab02_gps_plate_motion.ipynb` — the notebook, with outputs and plots saved so they render on GitHub
- `lab02_gps_plate_motion.html` — a standalone HTML export of the executed notebook
- `data/positions.csv.gz` — trimmed GPS series (station, date, decimal date, north mm, east mm)
- `data/stations.csv` — station metadata taken from the workbook headers
- `data/excel_reference.xlsx` — the 5-year difference, rate, and total-rate values from the completed spreadsheet, used by the check cell
- `data/excel_reference.csv` — the same reference values as a CSV
- `figures/` — PNG copies of the plots
- `requirements.txt` — Python dependencies

The original Excel workbook is not in this folder. It is large, and most of it is a date-conversion formula on every row. The trimmed CSV keeps only the columns the notebook uses.

### Figures

- `part1_timeseries.png` — BEMT and SBCC north and east vs decimal date, with the five-year window marked
- `part1_vectors.png` — north, east, and resultant arrows for BEMT and SBCC
- `part1_schematic_map.png` — schematic placement of those two vectors (BEMT's longitude is not in the workbook)
- `part3_timeseries.png` — CARH, CAND, and P294 north and east vs decimal date
- `part3_vectors.png` — north, east, and resultant arrows for the three Part 3 stations
- `part3_map.png` — the three stations in a local km frame, with velocity vectors to scale
- `summary_rates.png` — five-year horizontal rates at all five stations
- `extra_twopoint_vs_fit.png` — two-point rate vs a linear fit (extra, not in the lab)

## How to run

From this folder:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
pip install jupyter
jupyter notebook lab02_gps_plate_motion.ipynb
```

To re-execute the notebook from the command line and refresh the HTML copy:

```bash
pip install jupyter nbconvert ipykernel
jupyter nbconvert --to notebook --execute --inplace lab02_gps_plate_motion.ipynb
jupyter nbconvert --to html lab02_gps_plate_motion.ipynb
```
