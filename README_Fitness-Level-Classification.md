# Fitness Level Classification

## Overview

This project applies machine learning classification to categorize physical fitness levels based on participant characteristics and fitness test results.

The analysis uses a dataset containing 169 observations of participants aged 10–13 years. The target variable, **fitness result**, consists of five categories: `Baik`, `Baik Sekali`, `Cukup`, `Kurang`, and `Kurang Sekali`.

The project focuses on comparing several classification algorithms and evaluating their performance after handling class imbalance with SMOTE.

## Objectives

- Explore the distribution and characteristics of the fitness dataset.
- Prepare categorical and numerical variables for machine learning.
- Handle class imbalance using SMOTE.
- Compare multiple classification algorithms.
- Evaluate models using Accuracy, weighted F1-score, confusion matrices, and 5-fold cross-validation.
- Examine feature importance from the selected Random Forest model.

## Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)
- XGBoost

## Dataset

The original dataset contains 169 observations and 8 variables used in the analysis:

- Age
- Gender
- Test time
- Fitness result
- Exercise frequency
- Exercise heart rate
- Core exercise duration
- Type of physical exercise

For the classification model, the predictor variables are:

- Age
- Gender
- Test time

The target variable is:

- Fitness result

> **Data note:** The original dataset is not included in this repository unless a public/anonymized version is available and permitted for sharing. The notebook can be run after placing an appropriate dataset in the expected data path.

## Methodology

1. Data loading
2. Exploratory Data Analysis (EDA)
3. Data quality checking
4. Label encoding
5. Train-test split with stratification
6. Robust scaling
7. Handling class imbalance with SMOTE
8. Model training
9. Model comparison
10. Confusion matrix evaluation
11. 5-fold cross-validation
12. Feature importance analysis

## Models

The project compares:

- Decision Tree
- Random Forest
- K-Nearest Neighbors (KNN)
- Logistic Regression
- XGBoost

## Model Evaluation

The original notebook run reported the following 5-fold cross-validation results:

| Model | Mean Accuracy | Mean F1 |
|---|---:|---:|
| Decision Tree | 0.8492 | 0.8503 |
| Random Forest | 0.9639 | 0.9637 |
| KNN | 0.8984 | 0.8978 |
| Logistic Regression | 0.7607 | 0.7612 |
| XGBoost | 0.9377 | 0.9378 |

The original workflow selected **Random Forest** for the subsequent prediction and feature-importance analysis.

On the held-out test set, Random Forest achieved an accuracy of **0.9118** and weighted F1-score of **0.8875** in the recorded run.

These results are specific to the dataset split and preprocessing configuration used in the notebook and should not be interpreted as general performance on other populations.

## Repository Structure

```text
Fitness-Level-Classification/
│
├── README.md
│
└── notebook/
    └── fitness_level_classification.ipynb
```

## Notes

This project is presented as a portfolio demonstration of data preprocessing, imbalanced-class handling, supervised machine learning, model evaluation, and interpretation.

The exercise recommendations included in the original analysis are treated as project-specific outputs and are not presented as medical or clinical advice.
