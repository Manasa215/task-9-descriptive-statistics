# Task 9 — Descriptive Statistics Primer

**Program:** Veda Technology — HI T – Data Analytics Track  
**Level:** 1 · Day 9

## Objective
Calculate and interpret mean, median, mode, standard deviation, and percentiles for key numeric columns.

## Dataset
`titanic_style_practice_dataset.csv` is a **synthetic Titanic-style practice dataset** created for this task. It is not the original Titanic dataset. It contains 120 rows, five numeric analysis columns (Age, Fare, SibSp, Parch, Pclass), and a PassengerID identifier. Three Age values are intentionally missing.

## Project structure
- `data/` — practice dataset CSV
- `notebooks/` — Jupyter notebook using Pandas
- `reports/descriptive_statistics_workbook.xlsx` — Excel workbook with raw data and summary table
- `reports/summary_statistics.csv` — exported statistics
- `reports/findings_report.md` — interpretations, conclusion, and interview answers
- `evidence/` — reserved for screenshots of your own notebook/workbook run

## How to use
1. Download or clone this repository.
2. Open the project folder in VS Code.
3. Open `notebooks/task9_descriptive_statistics.ipynb` in VS Code and select a Python kernel with `pandas` installed.
4. Run the notebook cells from top to bottom.
5. Open the Excel workbook in `reports/` to review the raw data and statistics.
6. Read `reports/findings_report.md` for the interpretation and interview answers.

If Pandas is not installed in your selected environment, run `python -m pip install pandas jupyter` in the VS Code terminal.

## Main findings
- Mean and median comparisons help flag possible skew.
- Standard deviation measures spread around the mean and is sensitive to outliers.
- Q1 and Q3 define the middle 50%; IQR is Q3 minus Q1.
- Fare is right-skewed in this synthetic practice dataset.
- Pclass is categorical coding; interpret its numeric mean cautiously.

## Important note
This is a learning exercise using synthetic data. Do not claim the results describe real Titanic passengers. The evidence folder is initially empty; if your internship requires screenshots, run the notebook/workbook and add genuine screenshots of your own execution.
