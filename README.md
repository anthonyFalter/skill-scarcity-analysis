# Skill Scarcity Analysis

This repository analyzes how scarce specific skills are in the labor market, using the Datamata Studios Skill Scarcity Index dataset. The analysis compares supply and demand for skills, and explores trends by duration, job postings, and skill categories. This project is free for anyone to modify, or use in any of your personal interests. This is my personal project that showcases my skills in data analysis using advanced data analytics.

The project contains a clear and concise step by step of my thought process when creating the project, which you can use as a reference when doing your very own personal projects. If you have inquiries or changes that you want to push, feel free to fork or direct message me on my socials.

## Contents

- `01_eda.ipynb` — exploratory data analysis and initial visualizations
- `03_preprocessing.ipynb` — data cleaning, null value removal, and feature preparation for linear regression
- `02_hypothesis_testing.ipynb` — linear regression modeling with scaled features and encoded categoricals
- `dataset/raw/skill-scarcity-index.csv` — original dataset source file
- `dataset/processed/` — cleaned and transformed dataset outputs
- `figures/` — visualizations generated from the analysis
- `notebooks/` — main folder for python notebooks.

## Dataset

Source: Datamata Studios
Link: https://www.datamatastudios.com/datasets/skill-scarcity-index

### Column Metadata

| Column | Type | Description |
|--------|------|-------------|
| `snapshot_date` | date | UTC date the snapshot was computed (YYYY-MM-DD). |
| `category` | string | Job category: data, engineering, product, devops, security or ai. |
| `skill_name` | string | Canonical skill name from the extraction taxonomy. |
| `demand_count` | integer | Active listings mentioning the skill on the snapshot date. |
| `demand_pct` | number | demand_count as a percentage of all active listings in the category. |
| `median_days_open` | number | Median days recently-closed listings with this skill stayed open. Blank below the sample floor. |
| `salary_premium_pct` | number | Median disclosed salary of listings with this skill vs the category median, in percent. Blank below the sample floor. |
| `repost_rate_pct` | number | Share of this skill's listings that are re-posts of an earlier identical role (a failed-hire signal). |
| `scarcity_score` | number | 0-100 weighted percentile-rank composite within the category. Higher = harder to hire. |

## Usage

1. Clone this repository:

```powershell
git clone https://github.com/anthonyFalter/skill-scarcity-analysis.git
cd skill-scarcity-analysis
```

2. Open the notebooks in Jupyter or your preferred notebook environment.

3. Run the notebooks in order:

- `01_eda.ipynb`
- `03_preprocessing.ipynb`
- `02_hypothesis_testing.ipynb`

## Notes

- If you want to rerun the analysis, make sure the dataset file exists in `dataset/raw/`.
- Save any generated plots to `figures/` and cleaned outputs to `dataset/processed/`.
- Preprocessing drops rows with null values in `median_days_open` and `salary_premium_pct` for modeling.
- Feature encoding and scaling are applied to prepare data for linear regression analysis.
