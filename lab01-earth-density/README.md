# Lab 1 — Earth's Density: Constraining Planetary Interiors

Python reproduction of ERTH 2001 Lab 1, originally completed as an Excel spreadsheet. The notebook walks through the lab step for step: four concentric shells, a thickness-weighted average, spherical-shell volumes, seismic layer thicknesses, a forward-modeled density structure near 5.5 g/cm³, and Dante's hollow-Earth variant. Each step also has a 3D hemisphere cutaway of the shells, drawn to scale and colored by density on one shared color scale. A short extra section at the end compares the Step 4 shells to PREM averages; that comparison is not part of the original lab.

The notebook explains the concept of each step. It does not include answers to the lab's graded questions.

AI used: Python notebook built with help from an AI coding agent.

## Files

- `lab01_earth_density.ipynb` — the notebook, with outputs and plots saved so they render on GitHub
- `lab01_earth_density.html` — a standalone HTML export of the executed notebook
- `figures/` — PNG copies of the plots
- `requirements.txt` — Python dependencies

### Figures

- `step1_thickness_density.png` — Step 1 thickness and density pies
- `step1_cutaway.png` — Step 1 hemisphere cutaway (equal shells)
- `step2_thickness_volume.png` — Step 2 thickness and volume pies
- `step2_cutaway.png` — Step 2 cutaway (same geometry as Step 1)
- `step3_thickness_volume.png` — Step 3 thickness and volume pies
- `step3_cutaway.png` — Step 3 cutaway (seismic radii)
- `step4_volume_mass.png` — Step 4 volume and mass pies
- `step4_cutaway.png` — Step 4 cutaway (adjusted densities)
- `dante_thickness_volume.png` — Dante two-layer thickness and volume pies
- `dante_cutaway.png` — Dante cutaway, with the 1,000 km hollow at the center
- `summary_density_mass.png` — average density and mass of every model
- `summary_cutaways.png` — all five cutaways side by side, shared color scale
- `prem_vs_step4.png` — Step 4 densities vs PREM (extra, not in the lab)

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
