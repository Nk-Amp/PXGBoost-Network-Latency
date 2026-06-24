# PXGBoost-Basketball-Analytics
P-XGBoost: Feature-Pruned Defensive Matchup Evaluation
Project Description
This repository contains the proposed codebase for the research project "An Engineered Feature-Pruned XGBoost Model (P-XGBoost) for Evaluating Defensive Matchup Efficiency in Professional Basketball: A SHAP-Explainability Approach." The project implements an engineered variant of the XGBoost algorithm, which utilizes a mid-training callback to perform SHAP-guided dimensionality reduction. The model systematically prunes the bottom 30% of non-contributing kinematic variables during training to improve inference speed while maintaining predictive accuracy, specifically for evaluating basketball defensive isolation matchups.

Repository Contents
/data: Placeholder for defensive isolation possession logs (KNUST Sports Analytics Research Data) and processed NBA tracking statistics.

/notebooks: Contains the training pipeline, SHAP-based pruning logic, and evaluation scripts for comparing P-XGBoost against standard baseline models.

/src: Modular Python scripts for data preprocessing and custom callback definitions.

Dependencies
The implementation relies on the following core Python libraries:

xgboost (v2.0.3 or higher)

shap (v0.44.0 or higher)

pandas

scikit-learn (v1.4 or higher)

Research Overview
This work is part of a Q1-journal submission track proposal. The P-XGBoost model aims to provide a lightweight, interpretable tool for real-time basketball defensive matchup evaluation, suitable for deployment on local devices in coaching environments.

License
This repository is associated with the Department of Computer Science, Kwame Nkrumah University of Science and Technology (KNUST). All rights reserved.
