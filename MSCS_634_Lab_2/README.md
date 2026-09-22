# MSCS 634 Lab 2 — Classification Using KNN and RNN

## Purpose

This lab compares K-Nearest Neighbors and Radius Neighbors classifiers using scikit-learn's Wine Dataset. It examines how k and radius affect test accuracy and explains when each classifier may be preferable.

## Files

- `MSCS_634_Lab_2.ipynb` — completed notebook with code, saved results, plots, and discussion
- `screenshots/` — saved dataset exploration, accuracy tables, and trend plots
- `build_lab2.py` — reproducibility script used to verify and rebuild the submission

## Requirement checklist

- Step 1: Wine Dataset loaded from `sklearn`; features and class distribution explored; stratified 80/20 split performed.
- Step 2: KNN trained and evaluated for k = 1, 5, 11, 15, and 21; every accuracy recorded.
- Step 3: RNN trained and evaluated for radii = 350, 400, 450, 500, 550, and 600; every accuracy recorded.
- Step 4: Separate KNN and RNN accuracy-trend plots, direct comparison, observations, and model-selection guidance included.

## Key insights

- KNN reaches 80.56% accuracy at k = 5, 11, 15, and 21; k = 1 reaches 77.78%.
- RNN performs best at radius 350 with 72.22% accuracy, then generally declines as radius increases.
- KNN is stronger for this split and parameter set. RNN may be useful when a domain provides a meaningful distance threshold or local density should control the number of voters.

## Challenges and decisions

The split uses `random_state=42` and `stratify=y` for reproducibility and class balance. The features remain unscaled because the assigned RNN radii of 350–600 are designed for the original feature units. RNN uses `outlier_label='most_frequent'` to define behavior for any sample with no neighbor inside the radius.

## Running the notebook

1. Open `MSCS_634_Lab_2.ipynb` in Jupyter.
2. Run the first setup cell to install `pandas`, `numpy`, `matplotlib`, and `scikit-learn` into the active kernel.
3. Restart the kernel if prompted, then choose Run All.

