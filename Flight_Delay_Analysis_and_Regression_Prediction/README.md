# Flight Delay Prediction: Regression (and Classification comment)

**Goal:** Evaluate whether flight departure delays can be accurately predicted as a regression problem, and provide a data‑driven recommendation for a more effective modelling approach.

## Overview

Flight delays cause substantial economic losses and passenger inconvenience. This project uses the **Flight Delay Dataset 2018–2024** (Kaggle) to predict departure delays. We built a feature engineering pipeline (rolling historical delays, airport congestion, carrier‑route interactions, time‑based features) with strict prevention of data leakage. Six regression models (Linear, Ridge, Lasso, Random Forest, XGBoost, Neural Network) were trained and evaluated.

This project tackles this challenge by analyzing a public dataset dowloaded from https://www.kaggle.com/datasets/shubhamsingh42/flight-delay-dataset-2018-2024. 


## Key Findings

- **Regression performed poorly**: All models achieved R² between 0.04 and 0.07, and MAE around 23–25 minutes. Random Forest and the Neural Network even produced negative R² (worse than predicting the mean).
- **The problem is inherently noisy**: External factors (weather, ATC, crew) make exact minute‑level prediction extremely difficult with the available data.
- **Classification is the better formulation**: Predicting whether a flight will be delayed (e.g., ≥15 minutes) is both more accurate and more actionable. Academic benchmarks and community examples (e.g., the Kaggle notebook “✈️ Flight Delay Analysis 2018–2024”) report ROC‑AUC >0.95 and accuracy >80% for binary delay classification.
