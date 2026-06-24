# P-XGBoost: Network Latency Spike Prediction

## Project Description
This repository contains the codebase for the research project **"An Engineered Feature-Pruned XGBoost Model (P-XGBoost) for Predicting High-Severity Latency Spikes in Mobile Gaming Networks."** This project introduces a two-stage training pipeline that uses an initial SHAP-based probing stage to identify the most predictive network features, followed by an iterative pruning stage to remove the bottom 30% of noise-contributing variables. The final pruned ensemble model provides a low-latency predictive engine suitable for edge-device deployment.

## Repository Contents
* **/data**: Contains the merged dataset consisting of the **UNSW-NB15** network traffic benchmark and primary telemetry logs collected from local mobile gaming sessions.
* **/notebooks**: 
    * `01_baseline_training.ipynb`: Training and benchmarking of standard XGBoost.
    * `02_shap_pruning_pipeline.ipynb`: Implementation of the SHAP-guided iterative pruning logic and secondary model training.
* **/src**: 
    * `callbacks.py`: Custom logic for model checkpointing to Google Drive every 50 boosting rounds.
    * `preprocessing.py`: Data scaling and SessionID-based data splitting.

## Dependencies
The implementation relies on:
* `xgboost` (v2.0.3)
* `shap` (v0.44.0)
* `pandas`, `scikit-learn` (v1.4)
* `optuna` (for hyperparameter tuning)

## Research Overview
This model is engineered for real-time latency prediction in mobile network environments, optimizing for an AUC-PR metric. It targets deployment on mobile edge devices where CPU overhead must be minimized.

## License
Department of Computer Science, KNUST. All rights reserved.
