# System Threat Prediction (MLP Project)

A binary classifier that predicts whether a machine is at risk of a threat from its system telemetry.

## Why this exists
Kaggle competition project for the Machine Learning Practice course in the IIT Madras BS in Data Science (course grade: S).

## What it does
- Cleans the data: missing values, low-variance and high-null columns, skewed numbers
- Encodes categorical features and adds time-based and count features
- Compares logistic regression, random forest, XGBoost and LightGBM
- Handles class imbalance with SMOTE and class weights
- Tunes with GridSearchCV and Optuna, evaluating AUC-ROC, F1 and accuracy on stratified folds
- Writes the competition submission from the final model

## Project structure
```
mlp_project/
├── milestone.ipynb … milestone4.ipynb  Graded milestone submissions
├── final.ipynb                         Final model and submission
├── file*.ipynb, stand.ipynb            Experiments
├── train.csv                           Training data with labels
├── test.csv                            Data to predict
└── sample_submission.csv               Submission format
```

## Getting started
Requirements: Python 3.10+, Jupyter.
```bash
git clone https://github.com/abhijha8287/mlp_project.git
cd mlp_project
pip install jupyter pandas numpy scikit-learn xgboost lightgbm imbalanced-learn optuna
jupyter notebook final.ipynb
```

## Tech stack
Python, scikit-learn, XGBoost, LightGBM, imbalanced-learn, Optuna, pandas, Jupyter

## Notes
Target column: `is_threat` (1 = threat, 0 = safe).
