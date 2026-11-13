# Lab 3 — Density and Isostasy

Python reproduction of ERTH 2001 Lab 3, originally completed as an Excel workbook plus written calculations. The notebook walks through the lab step for step: average densities of basalt, granite, and peridotite from mass and volume samples; a plot of stranded-beach height versus age at Hudson Bay, with linear and quadratic fits to the postglacial rebound; and a floating-block (Airy-style) calculation of how high oceanic and continental crust sit in the mantle, compared with Earth's bimodal topography, and of how thick the crust is under the Andes. A short extra section compares the spreadsheet's mean-of-ratios density with the bulk ratio of total mass to total volume; that comparison is not part of the original lab.

The notebook explains the concept of each step: every code cell has a plain-language introduction before it and a short "what this shows" after it. It does not include answers to the lab's graded questions.

AI used: Python notebook built with help from an AI coding agent.

## Files

- `lab03_density_isostasy.ipynb` — the notebook, with outputs and plots saved so they render on GitHub
- `lab03_density_isostasy.html` — a standalone HTML export of the executed notebook
- `data/rock_samples.csv` — ten mass-and-volume samples each of basalt, granite, and peridotite
- `data/hudson_bay_beaches.csv` — height (m) and age (yr BP) of 19 stranded beaches
- `data/excel_reference.xlsx` — the three average-density values from the completed spreadsheet, used by the check cell
- `data/excel_reference.csv` — the same reference values as a CSV
- `figures/` — PNG copies of the plots
- `requirements.txt` — Python dependencies

The original Excel workbook is not in this folder. The trimmed CSVs keep the columns the notebook uses.

### Figures

- `part1_sample_densities.png` — the ten sample densities of each rock type, with their means
- `part2_beaches.png` — Hudson Bay beach height versus age
- `part2_fits.png` — the same points with a linear fit and a quadratic fit
- `part2_residuals.png` — residuals of those two fits
- `part3_floating_blocks.png` — 5 km of basalt and 30 km of granite floating in the mantle, to vertical scale
- `part3_south_america_section.png` — schematic east–west section with the Andes root
- `extra_two_averages.png` — mean-of-ratios density vs bulk density (extra, not in the lab)

## How to run

From this folder:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
pip install jupyter
jupyter notebook lab03_density_isostasy.ipynb
```

To re-execute the notebook from the command line and refresh the HTML copy:

```bash
pip install jupyter nbconvert ipykernel
jupyter nbconvert --to notebook --execute --inplace lab03_density_isostasy.ipynb
jupyter nbconvert --to html lab03_density_isostasy.ipynb
```
