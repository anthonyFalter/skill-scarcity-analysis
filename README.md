# Skill Scarcity Analysis

This repository analyzes how scarce specific skills are in the labor market, using the Datamata Studios Skill Scarcity Index dataset. The analysis compares supply and demand for skills, and explores trends by duration, job postings, and skill categories.

## Contents

- `01_eda.ipynb` — exploratory data analysis and initial visualizations
- `02_preprocessing.ipynb` — data cleaning and feature preparation
- `dataset/raw/skill-scarcity-index.csv` — original dataset source file
- `dataset/processed/` — cleaned and transformed dataset outputs
- `figures/` — visualizations generated from the analysis
- `preprocessing/` — helper scripts or modules used for data preparation

## Dataset

Source: Datamata Studios
Link: https://www.datamatastudios.com/datasets/skill-scarcity-index

## Usage

1. Clone this repository:

```powershell
git clone https://github.com/anthonyFalter/skill-scarcity-analysis.git
cd skill-scarcity-analysis
```

2. Open the notebooks in Jupyter or your preferred notebook environment.

3. Run the notebooks in order:

- `01_eda.ipynb`
- `02_preprocessing.ipynb`

## Notes

- If you want to rerun the analysis, make sure the dataset file exists in `dataset/raw/`.
- Save any generated plots to `figures/` and cleaned outputs to `dataset/processed/`.
