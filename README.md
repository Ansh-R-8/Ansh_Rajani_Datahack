# Predict Vaccination outcomes

## Overview

This file contains Python code for training a machine learning model to predict vaccination outcomes based on survey data. 
It utilizes XGBoost as the classifier and includes preprocessing steps such as imputation and scaling.

## Contents

1. **Data Preprocessing**:
   - Missing value imputation using median for numerical features.
   - Most frequent imputation and one-hot encoding for categorical features.
   - Scaling of numerical features using StandardScaler.

2. **Model Training**:
  - **XGBoost Classifier**:
     - Utilizes Gradient Boosting framework for ensemble learning.
     - Hyperparameter tuning using GridSearchCV for optimal model performance
     - Prediction of two vaccine outcomes simultaneously: `xyz_vaccine` and `seasonal_vaccine`.
       
3. **Evaluation**:
   - Evaluation metric used: ROC AUC score.
   - Prediction probabilities are computed and saved to a CSV file (`submission.csv`).
   - Model performance is assessed using the ROC AUC score on a held-out test set for XGBoost classifier.
  
  ## Files Included

- `training_set_features.csv`: Contains the features used for training.
- `training_set_labels.csv`: Contains the corresponding labels for training.
- `submission_xgboost.csv`: Output file containing predicted probabilities by XGBoost.
- `test_set_features.csv`: Contains the corresponding labels for training.

