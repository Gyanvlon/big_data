# MSCS 634 Lab 6 — Apriori and FP-Growth

## Purpose

This lab mines frequent itemsets and association rules from a cleaned subset of the public UCI Online Retail dataset using Apriori and FP-Growth, then explains the patterns with Seaborn visualizations.

Source: https://archive.ics.uci.edu/dataset/352/online+retail

## Files

- `MSCS_634_Lab_6.ipynb` — completed notebook with saved outputs, visualizations, and analysis
- `online_retail_transactions.csv` — cleaned item-level UCI-derived transactional subset
- `screenshots/` — preparation, item frequency, co-occurrence, itemsets, rules, and comparison evidence
- `build_lab6.py` — reproducibility and verification script

## Requirement checklist

- Step 1: Public transactional data loaded and cleaned; baskets encoded; Seaborn item-frequency bar plot and co-occurrence heatmap included.
- Step 2: Apriori uses 3% support; supports displayed; top-itemset Seaborn bar plot included.
- Step 3: FP-Growth uses the same support; output and runtime compared; top-itemset bar plot included.
- Step 4: Rules use 55% confidence; support, confidence, and lift displayed and interpreted; confidence-vs-lift scatter plot included.
- Step 5: Outputs, timing, algorithm behavior, parameter decisions, and challenges compared.

## Key insights

- Both algorithms return 307 identical frequent itemsets and 59 rules at the selected thresholds.
- Coordinated designs such as GREEN/ROSES REGENCY teacup-and-saucer products show strong positive association.
- Apriori was faster in the verified run (0.009733s versus 0.026368s) because the filtered basket matrix is modest; FP-tree overhead dominates here.

## Challenges and decisions

Cleaning removed cancellations and invalid rows. The analysis retains the 100 most frequent items and multi-item baskets to control combinatorial growth. A 3% support threshold balances useful patterns with readable output. Postage-related rules are flagged as operational rather than automatically actionable.
