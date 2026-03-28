Cisco Forecast League 2026 – Phase 1

# Cisco Forecast League 2026 – Phase 1

## Overview
This repository contains our team project for Phase 1 of the Cisco Forecast League 2026.  
We built a hybrid forecasting pipeline that blends statistical methods with machine learning approaches to generate forecasts across 30 products.

---

## Data Preparation
We worked extensively with the provided External Data Pack (Excel sheets with multi‑level headers).  
Key preprocessing steps included:
- Flattening multi‑level column headers
- Cleaning column names and dropping empty columns
- Splitting data into actuals, forecasts, big deals, and SCMS units
- Reshaping wide tables into long format for easier modeling

**Example outputs:**
- `df_actuals` → shape `(66, 22)` after cleaning
- `df_forecasts` → shape `(61, 6)` with demand, marketing, and data science forecasts
- `df_big_long` → reshaped big deals data with cost rank, product, quarter, and values
- `df_scms` → shape `(174, 16)` with SCMS units across coverage categories

---

## Modeling Approach
We experimented with:
- XGBoost
- LightGBM
- Moving Average
- Naive Bayes

We then applied ensemble learning to combine outputs and improve robustness.

---

## Key Learnings
- Real‑world forecasting requires balancing accuracy with interpretability
- Ensemble methods capture diverse patterns but need careful tuning
- Data preprocessing is as critical as model selection

---

## Future Work
- Explore deep learning approaches (LSTMs, Transformers) for time series
- Automate hyperparameter tuning for ensembles
- Extend pipeline to handle larger product sets

