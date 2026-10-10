# MSCS 634 Lab 4 — Regression and Regularization

## Purpose

This lab compares simple linear, multiple linear, polynomial, Ridge, and Lasso regression on scikit-learn's Diabetes Dataset using MAE, MSE, RMSE, and R².

## Files

- `MSCS_634_Lab_4.ipynb` — completed notebook with saved outputs, visualizations, and analysis
- `screenshots/` — preparation, metrics, predictions, regularization, and comparison evidence
- `build_lab4.py` — reproducibility and verification script

## Requirement checklist

- Step 1: Dataset loaded and explored; missing values and duplicates checked; 80/20 split created.
- Step 2: BMI-only simple regression evaluated with all four metrics and visualized.
- Step 3: Multiple regression uses all ten features, reports all metrics, and plots actual versus predicted.
- Step 4: Polynomial degrees 1–3 compare train/test behavior and demonstrate overfitting.
- Step 5: Ridge and Lasso evaluate several alpha values with identical metrics and prediction plots.
- Step 6: A final table and written analysis compare performance, overfitting, and dataset insights.

## Key insights

- Multiple regression improves test R² from 0.233 to 0.453 over the BMI-only model.
- Degree-3 polynomial regression overfits badly: training R² is 0.857, while test R² is -5.212.
- Lasso α=1 is the best tested configuration with R² 0.467 and RMSE 53.15.

## Challenges and decisions

One consistent split (`random_state=42`) supports fair comparison. Polynomial features use all predictors so increasing degree clearly demonstrates variance and overfitting. Ridge and Lasso are placed after `StandardScaler` so alpha penalizes coefficients on a common scale.

