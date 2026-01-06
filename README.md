
# final-project-Shahid-hussain
# Hepatitis C Prediction Using Supervised Machine Learning

This project builds and evaluates supervised machine learning models to
predict **Hepatitis C disease status/stage** using demographic and
biochemical liver biomarker data. The workflow includes preprocessing,
EDA, model training, grid search with cross-validation, and evaluation.

## Overview

Hepatitis C often progresses silently; non-invasive prediction from
routine labs may support early screening.

Models compared: - Logistic Regression\
- Decision Tree\
- Random Forest\
- Gradient Boosting

## Dataset

-   Public dataset from **UCI Machine Learning Repository** containing
    Blood Donors and Hepatitis C patients (Hepatitis, Fibrosis,
    Cirrhosis).\
-   Features: Age, Sex, ALB, ALT, AST, ALP, GGT, Bilirubin, Cholesterol,
    Proteins, etc.\
-   Data is **highly imbalanced** toward donor class.

## Methodology

### Preprocessing

-   Cleaning and formatting\
-   Missing value imputation (median for skewed numerical, mode for
    categorical)\
-   Categorical encoding\
-   Outlier review with IQR/Z-score\
-   Feature scaling after 80/20 stratified split

### Exploratory Analysis

-   Boxplots & histograms\
-   Correlation heatmap showing relationships among enzymes and proteins

### Optimization

-   Grid Search + k-fold CV for robust hyperparameters

### Evaluation Metrics

-   Accuracy, Precision, Recall, F1-score\
-   Confusion Matrix (macro focus)

## Key Findings

Important biomarkers: **ALT, AST, GGT, Albumin, Bilirubin**.\
Ensemble models gave better minority-class balance than linear baseline.

## Limitations

-   Single dataset\
-   Imbalance may inflate accuracy\
-   Need external validation & explainability (e.g., SHAP)

## Structure (suggested)

    ├── data/raw
    ├── notebooks
    ├── src
    └── outputs

## Requirements

Python 3.9+

    numpy
    pandas
    scikit-learn
    matplotlib
    seaborn

## Usage

    pip install -r requirements.txt
    python src/HepatisisC_Models.ipynb

## Ethics

Data is anonymized and used only for educational research.

------------------------------------------------------------------------

## License

This dataset is licensed under a **Creative Commons Attribution 4.0
International (CC BY 4.0)** license.

This allows sharing and adaptation of the dataset for any purpose,
provided that appropriate credit is given.
