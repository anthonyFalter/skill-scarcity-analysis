# Skill Scarcity Analysis

This repository analyzes how scarce specific skills are in the labor market, using the Datamata Studios Skill Scarcity Index dataset. The analysis compares supply and demand for skills, and explores trends by duration, job postings, and skill categories. This project is free for anyone to modify, or use in any of your personal interests.

## Contents

- `01_eda.ipynb` — exploratory data analysis and initial visualizations
- `02_preprocessing.ipynb` — data cleaning and feature preparation
- `03_hypothesis_testing.ipynb` — statistical modelling, conclusions that back the evidences found during EDA.
- `dataset/raw/skill-scarcity-index.csv` — original dataset source file
- `dataset/processed/` — cleaned and transformed dataset outputs
- `figures/` — visualizations generated from the analysis
- `preprocessing/` — helper scripts or modules used for data preparation


Column	Type	        Description
`snapshot_date`	        date	UTC date the snapshot was computed (YYYY-MM-DD).
`category`	            string	Job category: data, engineering, product, devops, security or ai.
`skill_name`	        string	Canonical skill name from the extraction taxonomy.
`demand_count`	        integer	Active listings mentioning the skill on the snapshot date.
`demand_pct`	        number	demand_count as a percentage of all active listings in the category.
`median_days_open`	    number	Median days recently-closed listings with this skill stayed open. Blank below the sample floor.
`salary_premium_pct`	number	Median disclosed salary of listings with this skill vs the category median, in percent. Blank below the sample floor.
`repost_rate_pct`	    number	Share of this skill's listings that are re-posts of an earlier identical role (a failed-hire signal).
`scarcity_score`	    number	0-100 weighted percentile-rank composite within the category. Higher = harder to hire.

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
- `03_hypothesis_testing.ipynb`

## Notes

- If you want to rerun the analysis, make sure the dataset file exists in `dataset/raw/`.
- Save any generated plots to `figures/` and cleaned outputs to `dataset/processed/`.
