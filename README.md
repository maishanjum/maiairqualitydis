# maiairqualitydis
# Machine Learning Approaches to Urban Air Quality Prediction in Smart Cities: A Cross-Climate Study of New York City and Los Angeles

## Project Overview

This repository features a dissertation project examining short-term urban air quality forecasting through a cross-climate lens, comparing New York City (NYC) and Los Angeles (LA) using a unified machine learning pipeline. The study investigates how differences in climate and urban form affect both pollutant behavior and predictive model performance for key air pollutants ($PM_{2.5}$, $NO_2$, $O_3$, and $CO$) using data spanning from 2015 to 2025.

## Key Features & Methodology

* **Data Sources:** Utilizes daily data from the EPA Air Quality System (2015–2025) alongside NOAA and Kaggle climate data.
* **Preprocessing Pipeline:** Includes dataset harmonization, short-gap interpolation, Min-Max scaling for neural networks, and feature engineering with lagged pollutant variables and contextual inputs while preserving natural climate anomaly spikes (such as LA wildfires).
* **Machine Learning Models:** Evaluates and compares four distinct architectures:
* **Long Short-Term Memory (LSTM):** Target-optimized for capturing temporal dependencies and sequential patterns.
* **XGBoost:** High-performance gradient boosting optimized for tabular data structures.
* **Random Forest:** Robust ensemble approach providing strong baseline stability and feature tracking.
* **Feedforward Neural Network:** Deep learning baseline model.


* **Model Interpretability:** Incorporates **SHAP (SHapley Additive exPlanations)** and **LIME (Local Interpretable Model-agnostic Explanations)** to translate black-box model predictions into transparent, actionable insights for policy and urban planning.

## Key Findings & Performance

* **Context-Dependent Performance:** Tree-based ensembles (XGBoost, Random Forest) and LSTMs achieved high forecasting skills ($R^2$ scores generally ranging between $0.60$ and $0.88$ depending on the pollutant and city), with LSTMs particularly strong for capturing LA's climate-driven variations.
* **Driver Validation:** Correlation analysis confirmed that temperature is a primary driver for ground-level ozone ($O_3$) formation in warm climates like LA, whereas traffic-related pollutants ($NO_2$ and $CO$) showed weaker direct climate correlations, tying more heavily to urban transit and combustion density.
* **Feature Importance Insights:** SHAP metrics highlighted distinct regional dependencies—temperature and seasonal timing heavily influenced LA's wildfire-driven $PM_{2.5}$ and photochemical $O_3$, whereas traffic proxies dominated NYC's $NO_2$ and $CO$ predictions.

## Policy & Smart City Implications

* Demonstrates that a one-size-fits-all forecasting model is suboptimal for smart city applications.
* Suggests that NYC interventions should prioritize traffic management and heating infrastructure regulations to curb $NO_2$ and $CO$, while LA strategies must focus on climate adaptation, wildfire readiness, and ozone control.
