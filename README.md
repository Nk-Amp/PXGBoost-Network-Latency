# P-XGBoost: Feature-Pruned Latency Spike Prediction

## Project Description
This repository contains the codebase for the research project "An Engineered Feature-Pruned XGBoost Model (P-XGBoost) for Predicting High-Severity Latency Spikes in Mobile Gaming Networks." The project implements a two-stage training pipeline: Stage 1 (Probing) identifies high-impact network telemetry features via SHAP, and Stage 2 (Retraining) prunes the bottom 30% of features to optimize for edge-device inference latency.

## Repository Contents
* **/data**: Contains the UNSW-NB15 network traffic benchmark and primary telemetry logs collected from local gaming sessions.
* **/notebooks**: 
    * `01_baseline_training.ipynb`: Training and benchmarking of standard XGBoost.
    * `02_shap_pruning_pipeline.ipynb`: Implementation of the two-stage iterative pruning logic.
* **/src**: Modular Python scripts for data preprocessing and custom pruning callbacks.
* `requirements.txt`: Project dependencies and versioning.

## Research Overview
This model is engineered for real-time latency prediction in mobile network environments, optimizing for an AUC-PR metric and suitability for edge-device deployment.

## License
Department of Computer Science, KNUST. All rights reserved.
