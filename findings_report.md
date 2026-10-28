# Task 9 — Descriptive Statistics Primer

**Track:** HI T – Data Analytics Track, Veda Technology  
**Level:** 1 · Day 9  
**Tools:** Excel, Python, Pandas  
**Dataset:** Titanic-style synthetic practice dataset (120 rows)

## 1. Objective
Calculate and interpret mean, median, mode, standard deviation, and percentiles for key numeric columns. Use these statistics to describe typical values, spread, and possible skew.

## 2. Dataset and preparation
This project uses a **synthetic Titanic-style practice dataset**, not the original passenger manifest. It contains 120 rows and the numeric columns Age, Fare, SibSp, Parch, and Pclass, along with PassengerID. Three Age values are intentionally missing to demonstrate how pandas handles missing observations. PassengerID is an identifier and is excluded from interpretation.

## 3. Summary statistics
The workbook `descriptive_statistics_workbook.xlsx` contains the raw data and a summary table. The CSV version is also included at `summary_statistics.csv`.

| Column | Count | Mean | Median | Mode | Sample SD | Q1 (25%) | Q2 (50%) | Q3 (75%) | IQR |
|---|---:|---:|---:|---|---:|---:|---:|---:|---:|
| Age | 117 | 28.76 | 28.10 | 0.5 | 13.98 | 19.70 | 28.10 | 38.20 | 18.50 |\n| Fare | 120 | 39.67 | 24.38 | 4.0, 250.0 | 49.20 | 12.48 | 24.38 | 49.64 | 37.16 |\n| SibSp | 120 | 0.40 | 0.00 | 0 | 0.80 | 0.00 | 0.00 | 1.00 | 1.00 |\n| Parch | 120 | 0.38 | 0.00 | 0 | 0.82 | 0.00 | 0.00 | 0.00 | 0.00 |\n| Pclass | 120 | 2.29 | 3.00 | 3 | 0.83 | 2.00 | 3.00 | 3.00 | 1.00 |\n
## 4. Interpretation and findings

- **Age:** Mean = 28.76, median = 28.10. The mean is higher than the median, suggesting some right-skew in this sample. The standard deviation (13.98) indicates how much ages vary around the mean. The middle 50% of observed ages lie between Q1 = 19.70 and Q3 = 38.20.
- **Fare:** Mean = 39.67, median = 24.38. The mean is higher than the median, consistent with a **right-skewed** distribution where a smaller number of high fares pull the mean upward. The IQR (37.16) describes the spread of the middle half, while the standard deviation (49.20) reflects overall variability and is sensitive to extreme values.
- **SibSp:** The median is 0.00 and mode is 0. These values describe the most typical number of siblings/spouses aboard; the distribution is concentrated at low counts.
- **Parch:** The median is 0.00 and mode is 0. This indicates that many practice records have zero or few parents/children aboard.
- **Pclass:** This is a coded category (1, 2, 3), so mean and standard deviation can be calculated but should be interpreted cautiously. Frequencies and the mode are more meaningful for describing which class is most common.

### Overall conclusion
Mean and median together help identify possible skew; standard deviation describes spread around the mean; and percentiles show where observations fall in the distribution. For skewed data such as Fare, the median and IQR are often more representative than the mean and standard deviation alone. Statistics describe this synthetic sample only and should not be presented as findings about actual Titanic passengers.

## 5. Key concepts
- **Mean:** Sum of values divided by the number of non-missing observations; sensitive to extreme values.
- **Median:** Middle value after sorting; resistant to outliers and useful for skewed data.
- **Mode:** Most frequent value; useful for identifying the most common value or category.
- **Standard deviation:** Typical scale of variation around the mean; a larger value means observations are more spread out in the same units as the variable.
- **Percentiles:** A percentile is a value below which a given percentage of observations falls. Q1, Q2, and Q3 are the 25th, 50th, and 75th percentiles.
- **IQR:** Q3 − Q1; spread of the middle 50% of the observations.

## 6. Interview questions and answers

**Q1. When is median a better measure of center than mean?**  
The median is better when data is skewed or contains extreme values, because it is less affected by outliers. For example, income or fare data may contain a few very large values that pull the mean upward.

**Q2. What does a large standard deviation tell you about a dataset?**  
It tells us the values are widely spread around the mean. Standard deviation should be interpreted with the mean and the variable's units, and it can be inflated by outliers or skew.

## 7. Limitations
This is a small synthetic dataset designed for learning and reproducibility. The results are illustrative, not historical or scientific conclusions about the Titanic. Pandas excludes missing values from each statistic by default; the Age count is therefore lower than the total row count.
