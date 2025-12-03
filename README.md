# IPL Analysis Project

**Data Science project analyzing IPL player & team performance with visualizations and simple ML models.**  
This repository contains a cleaned notebook, charts, and a short write-up of insights and model results.

---

## Project Overview

**Goal:** Analyze IPL player and team performance, visualize key findings (top batsmen, team win % by season, venue scoring patterns), and build simple ML models to predict a player's total runs in a season.

**Dataset:** Match-level and player-level data (CSV files) — aggregated to season / player level for modeling and visualization.

---


---

## Quick Findings (EDA)

- **Top batsmen:** AB de Villiers and other top 4 players lead by a large margin — consistent high performers across seasons.  
- **Team performance:** Sunrisers Hyderabad, Mumbai Indians and Rajasthan Royals show the highest win percentages across seasons.  
- **Venue patterns:** M. Chinnaswamy and Wankhede show higher average totals (batting-friendly); MA Chidambaram and some others show lower averages (bowler-friendly).

*(See `images/` for the visualizations.)*

---

## Machine Learning Summary

- **Models used:** Linear Regression, Random Forest (scikit-learn)  
- **Target:** Total runs by a player in a season (regression).  
- **Results:** Both models performed poorly using only the basic features (e.g., `season` or simple aggregates).  
  - Linear Regression: underfitted (predictions clustered), high RMSE, negative/low R².  
  - Random Forest: slightly better but still high residual errors and misclassifications after thresholding.  
- **Conclusion:** The dataset lacks important features (innings played, strike rate, batting position, number of matches, recent form) required for robust predictions.

---

## How to run

1. Install requirements (example):
```bash
pip install -r requirements.txt
# or
pip install pandas numpy matplotlib seaborn scikit-learn




