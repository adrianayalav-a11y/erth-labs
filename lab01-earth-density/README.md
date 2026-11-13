# Lab 1 — Earth's Density: Constraining Planetary Interiors

Python reproduction of ERTH 2001 Lab 1, originally completed as an Excel spreadsheet. The notebook walks through the lab step for step: four concentric shells, a thickness-weighted average, spherical-shell volumes, seismic layer thicknesses, a forward-modeled density structure near 5.5 g/cm³, and Dante's hollow-Earth variant. A short extra section at the end compares the Step 4 shells to PREM averages; that comparison is not part of the original lab.

The notebook explains the concept of each step. It does not include answers to the lab's graded questions.

AI used: Python notebook built with help from an AI coding agent.

## Files

- `lab01_earth_density.ipynb` — the notebook, with outputs and plots saved so they render on GitHub
- `lab01_earth_density.html` — a standalone HTML export of the executed notebook
- `figures/` — PNG copies of the plots
- `requirements.txt` — Python dependencies

## How to run

From this folder:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
pip install jupyter
jupyter notebook lab01_earth_density.ipynb
```

To re-execute the notebook from the command line and refresh the HTML copy:

```bash
pip install jupyter nbconvert ipykernel
jupyter nbconvert --to notebook --execute --inplace lab01_earth_density.ipynb
jupyter nbconvert --to html lab01_earth_density.ipynb
```
