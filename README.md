# Bank Marketing – Term Deposit Subscription Prediction

## Project Overview

This project focuses on analysing bank marketing campaign data and building machine learning models to predict whether a customer will subscribe to a term deposit.

The main goal is to understand customer data, apply different classification algorithms and compare their performance, especially when dealing with an imbalanced dataset.

## Dataset

- **Dataset:** Bank Marketing (`bank-full.csv`)
- **Total Records:** 45,211
- **Total Columns:** 17
- **Target Variable:** `y` (yes/no)

The dataset contains customer information such as age, job, education, marital status, account balance, loans, contact details and previous campaign outcomes.

## Project Workflow

1. Data loading and understanding
2. Data checking and preprocessing
3. Target variable distribution analysis
4. Train-test splitting (80:20)
5. One-Hot Encoding for categorical features
6. Standard Scaling for numerical features
7. Building classification models
8. Model evaluation and comparison
9. Prediction threshold tuning
10. Handling class imbalance
11. Cross-validation
12. Hyperparameter tuning
13. Feature importance and feature selection

## Machine Learning Models

The following classification algorithms were implemented:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Gaussian Naive Bayes
- Linear Support Vector Classifier (SVM)
- Gradient Boosting
- XGBoost

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC-AUC
- Precision-Recall Curve
- Average Precision

## Model Results

The following results are from the standard model predictions on the test dataset. Precision, Recall and F1-score refer to customers who subscribed (`yes`).

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression | 89.33% | 66.32% | 17.86% | 28.15% |
| KNN | 88.19% | 49.00% | 24.00% | 32.00% |
| Decision Tree | 83.29% | 30.00% | 33.00% | 31.00% |
| Random Forest | 89.36% | 62.00% | 24.00% | 34.00% |
| Gaussian Naive Bayes | 84.52% | 37.00% | 46.00% | 41.00% |
| Linear SVC | 89.32% | 65.00% | 19.00% | 29.00% |
| Gradient Boosting | 89.43% | 66.00% | 20.00% | 31.00% |
| XGBoost | 89.47% | 67.00% | 20.00% | 31.00% |

## Handling Class Imbalance

The target variable contains an imbalance:

- No: 88.30%
- Yes: 11.70%

To understand its effect on model performance, different techniques were explored:

- Class Weight
- Random Oversampling
- Random Undersampling
- SMOTE

Different prediction thresholds were also tested to understand the trade-off between precision and recall.

## Hyperparameter Tuning and Cross-Validation

Decision Tree performance was further explored using:

- GridSearchCV
- RandomizedSearchCV
- Stratified K-Fold Cross-Validation

The best F1-score from RandomizedSearchCV was approximately 0.344 during cross-validation.

## Feature Importance and Selection

Decision Tree feature importance was used to identify important features.

Some of the important features included:

- Previous campaign outcome (`poutcome_success`)
- Account balance
- Age
- Contact day

Feature selection was also performed using `SelectFromModel`, reducing the feature set from 50 to 4 selected features.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- SciPy
- Imbalanced-learn
- XGBoost
- Jupyter Notebook

## Conclusion

This project helped me understand and apply different classification algorithms using bank marketing data. I also explored class imbalance, prediction thresholds, cross-validation and hyperparameter tuning.

One of the main observations was that accuracy alone is not enough to evaluate a classification model, especially when the target classes are imbalanced. Comparing precision, recall and F1-score helped me better understand how well each model identifies customers who actually subscribed to a term deposit.
