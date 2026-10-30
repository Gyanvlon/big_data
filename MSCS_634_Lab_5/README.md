# MSCS 634 Lab 5 — DBSCAN and Hierarchical Clustering

## Purpose

This lab compares Agglomerative Hierarchical Clustering and DBSCAN on the standardized Wine Dataset using parameter experiments, PCA visualizations, a dendrogram, and clustering-quality metrics.

## Files

- `MSCS_634_Lab_5.ipynb` — completed notebook with saved outputs and analysis
- `screenshots/` — exploration, experiments, clusters, dendrogram, and metrics
- `build_lab5.py` — reproducibility and verification script

## Requirement checklist

- Step 1: Wine Dataset loaded; `.head()`, `.info()`, and `.describe()` used; class distribution and missingness examined; features standardized.
- Step 2: Ward Agglomerative Clustering tested with 2–5 clusters; scatter plot and interpreted dendrogram included.
- Step 3: Eight DBSCAN parameter combinations tested; noise highlighted; Silhouette, Homogeneity, and Completeness reported.
- Step 4: Algorithms and parameter effects compared with strengths, weaknesses, and observations.

## Key insights

- Hierarchical n_clusters=3: Silhouette 0.2774, Homogeneity 0.7904, Completeness 0.7825.
- Selected DBSCAN (`eps=2.0`, `min_samples=3`) forms 5 clusters and marks 64 points as noise.
- Hierarchical clustering better represents the compact Wine groups; DBSCAN is highly sensitive to density parameters in 13 dimensions.

## Challenges and decisions

Standardization prevents large-scale features from dominating. PCA is used only for plotting; both algorithms and metrics use all standardized features. DBSCAN Silhouette excludes noise and is reported as unavailable when fewer than two non-noise clusters remain.


