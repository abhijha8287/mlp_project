# 🔐 System Threat Prediction - MLP Project (Kaggle Competition)

This repository contains my Machine Learning Practicum (MLP) project for predicting system-level threats in a classification setting. The project was built for a Kaggle competition and focuses on identifying malicious or suspicious behavior based on system activity data.

> 📌 **Goal:** Build a robust machine learning model that classifies whether a given system log represents a threat or not.

---

## 🧠 Problem Statement

System logs and telemetry data can help in proactively identifying threats like malware, intrusions, or abnormal behavior. The objective of this project was to develop a predictive model that:
- **Input:** Receives structured system data (e.g., process info, memory usage, file paths, etc.)
- **Output:** Predicts whether the system is under threat (`1`) or safe (`0`)

---

## 📊 Dataset Overview

- Provided by Kaggle as part of the competition.
- Contains anonymized logs of system activities.
- Key features:
  - Process names, paths, registry access
  - Memory and CPU usage stats
  - Event codes, timestamps
  - Target variable: `is_threat` (binary)

---

## ⚙️ Approach

### ✅ 1. Data Preprocessing
- Missing value handling
- Feature pruning: dropped features with low variance or high null count
- Label encoding / One-hot encoding for categorical features
- Log transformation of skewed numerical features
- Train-Test split without leakage

### ✅ 2. Feature Engineering
- Created new features from timestamps (hour, day, weekday)
- Extracted filename/domain info from path strings
- Count-based aggregation per user/session

### ✅ 3. Modeling
- Evaluated multiple classifiers:
  - Logistic Regression
  - Random Forest
  - XGBoost Classifier
  - LightGBM
- Applied class balancing (SMOTE / class_weight)
- Hyperparameter tuning using `GridSearchCV` and `Optuna`

### ✅ 4. Evaluation
- Metric used: **AUC-ROC**, **F1-score**, and **Accuracy**
- Cross-validation on stratified splits
- Confusion matrix analysis for false positives/negatives

---


