Cisco Forecast League 2026 – Phase 1

1) Overview
This repository contains Team Checkmate’s project for Phase 1 of the Cisco Forecast League 2026.
We built a hybrid forecasting pipeline that blends statistical methods with machine learning approaches to generate forecasts across 30 products.

2) Data Preparation
We worked extensively with the provided External Data Pack (Excel sheets with multi‑level headers).
Key preprocessing steps included:

-> Flattening multi‑level column headers.

-> Cleaning column names and dropping empty columns.

-> Splitting data into actuals, forecasts, big deals, and SCMS units.

-> Reshaping wide tables into long format for easier modeling.

Example outputs:

 a) df_actuals → shape (66, 22) after cleaning.

 b) df_forecasts → shape (61, 6) with demand, marketing, and data science forecasts.

 c) df_big_long → reshaped big deals data with cost rank, product, quarter, and values.

 d) df_scms → shape (174, 16) with SCMS units across coverage categories.

3) Modeling Approach
We experimented with:

XGBoost
LightGBM
Moving Average
Naive Bayes

We then applied ensemble learning to combine outputs and improve robustness.

4) Key Learnings
Real‑world forecasting requires balancing accuracy with interpretability.

Ensemble methods capture diverse patterns but need careful tuning.

Data preprocessing is as critical as model selection.

5) Future Work
  -> Explore deep learning approaches (LSTMs, Transformers) for time series.

  -> Automate hyperparameter tuning for ensembles.

  -> Extend pipeline to handle larger product sets.
