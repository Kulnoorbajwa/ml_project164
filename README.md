# CSCI 164 Final Project: Applied Machine Learning with scikit-learn

**Author:** Kulnoor Bajwa
**Course:** CSCI 164

## Overview

A supervised learning study across three datasets and three task types. The goal was to train and tune multiple algorithms on each dataset, compare their performance, and benchmark the results against published prior work. The project highlights how the best algorithm depends on the structure of the data and the type of prediction problem.

## Datasets

1. **Breast Cancer Wisconsin (Diagnostic)** for binary classification, sklearn built-in
2. **Optical Recognition of Handwritten Digits** for multi-class classification, sklearn built-in
3. **Diabetes Progression** for regression, sklearn built-in

All three datasets are bundled with scikit-learn and originally come from the UCI Machine Learning Repository, so no external CSV files are required.

## Models

| Dataset | Algorithms |
| --- | --- |
| Breast Cancer | Logistic Regression, k-NN, Random Forest, MLP |
| Digits | Logistic Regression, k-NN, MLP |
| Diabetes | Linear Regression, Ridge, k-NN, Decision Tree, MLP |

Every model was tuned with GridSearchCV using 5-fold cross-validation on an 80/20 train and test split. Preprocessing (StandardScaler) was wrapped in a Pipeline so that scaling happened inside each CV fold to prevent data leakage.

## Files

* `ml_project.ipynb`: full Jupyter notebook with code, outputs, plots, and analysis
* `ml_project_summary.pdf`: executive summary report
* `requirements.txt`: Python dependencies

## How to Run
pip install -r requirements.txt
jupyter notebook ml_project.ipynb

Then run all cells in order. Total runtime is roughly 3 to 5 minutes.

## Prior Work Cited

* Street, Wolberg, and Mangasarian (1993) for the Breast Cancer dataset
* Alpaydin and Kaynak (1998) for the Digits dataset
* Efron, Hastie, Johnstone, and Tibshirani (2004) for the Diabetes dataset
