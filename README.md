# MSCS 634 Lab 1 — Data Visualization, Preprocessing, and Statistical Analysis

## Purpose

This project demonstrates an end-to-end exploratory data analysis workflow in Python: loading data, visualizing patterns, handling missing values, detecting IQR outliers, reducing data, scaling and discretizing variables, and calculating descriptive statistics and correlations.

## Files

- `MSCS_634_Lab_1.ipynb` — completed notebook with code, explanations, and saved outputs
- `retail_sales_data.csv` — reproducible synthetic retail-sales dataset (72 orders)
- `screenshots/` — rubric evidence for the dataset preview, plots, preprocessing, and statistics

## Requirement checklist

- Data collection: CSV loaded with Pandas and the first five rows displayed.
- Visualization: monthly-revenue line plot and product-revenue bar chart, each with a written insight.
- Missing values: detection, affected rows, mean replacement, and before/after counts.
- Outliers: Q1, Q3, IQR, bounds, identified records, and post-removal size.
- Data reduction: column elimination plus reproducible 20% sampling, with before/after dimensions.
- Scaling and discretization: Min–Max scaling, Z-score standardization, and three sales bands.
- General statistics: `info()` and `describe()` outputs.
- Central tendency: minimum, maximum, mean, median, and mode.
- Dispersion: range, quartiles, IQR, variance, and standard deviation.
- Correlation: matrix for all numerical columns with interpretation.

## Key insights

- Laptop orders generate the most product revenue because of their higher unit price.
- Monthly revenue contains a visible spike caused by an unusually large order, demonstrating why outlier review matters.
- Five missing values were found (two discounts and three satisfaction scores) and replaced with numeric-column means.
- The 1.5×IQR rule identified two high `Units_Sold` outliers. They were removed only from `filtered_df`, preserving the original data.
- Revenue has a strong relationship with order size and is also influenced by unit price; correlations should be interpreted as association rather than causation.

## Decisions and challenges

The dataset was created with a fixed random seed so the analysis is reproducible and includes intentional missing values and outliers. Separate DataFrames are used at each preprocessing stage to avoid overwriting raw data. Mean imputation was chosen because missingness is limited; the IQR rule was chosen because it does not assume a normal distribution. A 20% sample and removal of low-value columns demonstrate reduction without changing the source file.

## Running the notebook

1. Place the notebook and CSV in the same directory.
2. Open the notebook in Jupyter and run the first code cell (`%pip install -q pandas numpy matplotlib`).
3. Restart the kernel if prompted, then choose **Kernel → Restart & Run All.
