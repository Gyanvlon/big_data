# MSCS 634 Lab 3 — K-Means and K-Medoids Clustering

## Purpose

This lab applies K-Means and K-Medoids clustering to the standardized Wine Dataset, evaluates both methods with the Silhouette Score and Adjusted Rand Index, and compares their cluster structures visually.

## Files

- `MSCS_634_Lab_3.ipynb` — completed notebook with code, saved outputs, plots, and analysis
- `screenshots/` — dataset preparation, metric outputs, comparison table, and cluster visualization
- `build_lab3.py` — reproducibility and verification script

## Requirement checklist

- Step 1: Wine Dataset loaded, features/classes explored, and all features standardized with z-scores.
- Step 2: K-Means implemented with k=3; labels, Silhouette Score, and ARI calculated.
- Step 3: K-Medoids implemented with k=3; medoids, labels, Silhouette Score, and ARI calculated.
- Step 4: Side-by-side PCA scatter plots include centroids/medoids; metrics and use cases are compared.

## Key insights

- K-Means: Silhouette Score = 0.2849; ARI = 0.8975.
- K-Medoids: Silhouette Score = 0.2676; ARI = 0.7411.
- K-Means forms better-defined clusters and aligns more closely with the known classes in this experiment.

## Challenges and decisions

Feature standardization prevents large-scale measurements from dominating distance. PCA is used only for the 2D plot; clustering and evaluation use all 13 standardized features. K-Medoids is implemented directly to make its assignment and medoid-update logic explicit and reproducible.

## Running 

Open the notebook, run its package setup cell, restart the kernel if prompted, and select Run All. 