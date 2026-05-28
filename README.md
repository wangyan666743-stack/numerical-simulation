# Numerical Simulation Data Repository

This repository is used to back up numerical simulation code, model outputs, processed results, and analysis notes for the thesis work.

## Directory Layout

- `src/`: simulation source files and model scripts.
- `scripts/analysis/`: reusable scripts for cleaning, plotting, and comparing results.
- `data/raw/`: original output files copied directly from each simulation run.
- `data/processed/`: cleaned tables, extracted indicators, and derived datasets.
- `runs/`: one folder per simulation run, including code snapshot, raw outputs, and a run manifest.
- `reports/`: analysis summaries, figures, and interpretation notes.
- `docs/`: project notes, parameter definitions, and method documentation.
- `metadata/`: run logs, data dictionaries, and index files.
- `templates/`: reusable templates for future simulation archiving.
- `notebooks/`: optional exploratory analysis notebooks.

## Run Archiving Rule

Each finished simulation should be saved as:

```text
runs/YYYYMMDD_short-name/
  manifest.yml
  code/
  raw/
  processed/
  figures/
  notes.md
```

The `manifest.yml` file records the model version, parameter scheme, input files, output files, and analysis status. Raw results should not be manually edited; cleaned or extracted data should be placed under `processed/`.

## Recommended Workflow

1. Copy the finished simulation code and raw outputs into a new folder under `runs/`.
2. Fill in `manifest.yml` from `templates/run_manifest.yml`.
3. Extract key indicators into `data/processed/` or the run-level `processed/` folder.
4. Add a short analysis note in `reports/` or the run-level `notes.md`.
5. Commit and push the changes to GitHub as a permanent backup.

