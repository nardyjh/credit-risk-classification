## Overview of the Analysis

### Purpose of the Analysis
The purpose of this analysis was to build and evaluate machine learning models for credit risk classification. The goal was to use historical lending data from a lending services company to predict the credit health of borrowers. The analysis aimed to develop models capable of distinguishing between healthy loans (class 0) and high-risk loans (class 1).

### Financial Information and Prediction
The dataset provided information on various financial features of loan applicants, such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The target variable for prediction was the "loan_status" column, where a value of 0 represented a healthy loan, and 1 indicated a high-risk loan.

### Variables and Stages of Machine Learning Process
  Variables to Predict:
  - Healthy Loans (Class 0)
  - High-Risk Loans (Class 1)
  
  Stages of Machine Learning Process:
    
  Data Loading and Exploration:
  - Checked basic information about the dataset, including variable types and missing values.
    
  Data Preprocessing:
  - Handled any missing data and converted categorical variables into numerical format.
    
  Data Splitting:
  - Split the dataset into training and testing sets for model training and evaluation.
    
  Original Model Training:
  - Trained a logistic regression model using the original (unbalanced) data.
  - Evaluated the model's performance using accuracy, precision, recall, and F1-score.
    
  Resampling:
  - Utilized the RandomOverSampler from imbalanced-learn to address class imbalance.
  - Resampled the training data to achieve a balanced distribution of classes.
    
  Model Training with Resampled Data:
  - Trained a logistic regression model using the resampled training data.
  - Evaluated the model's performance on the test set.

### Methods Used
  Logistic Regression:
  - Used logistic regression as the primary classification algorithm.
  Resampling:
  - Applied the RandomOverSampler to address class imbalance by oversampling the minority class.

### Results
  Machine Learning Model 1
  Original Logistic Regression Model:
  - Accuracy: 99.18%
  - Confusion Matrix:

  ```bash
  [[18663   102]
   [   56   563]]
  ```

  - Precision (Class 1): 85%
  - Recall (Class 1): 91%
  - F1-Score (Class 1): 88%

  Machine Learning Model 2
  Logistic Regression Model with Resampled Data:
  - Accuracy: 99.38%
  - Confusion Matrix:

  ```bash
  [[18649   116]
   [    4   615]]
  ```

  - Precision (Class 1): 84%
  - Recall (Class 1): 99%
  - F1-Score (Class 1): 91%

### Summary
  Model Performance Comparison
  Logistic Regression Model with Resampled Data (Model 2) Outperforms:
  - Higher accuracy (99.38% vs. 99.18%)
  - Improved precision, recall, and F1-score for high-risk loans (class 1).
  
  Recommendations
  Model Choice:
  - Logistic Regression Model with Resampled Data (Model 2)
  - Achieves higher accuracy and better performance in identifying high-risk loans.
  - The resampling technique enhances the model's ability to handle imbalanced data.
  Considerations:
  - The choice of the model may depend on the specific problem requirements.
  - If correctly identifying high-risk loans (class 1) is crucial, Model 2 is preferred.
  Overall Outcome:
  - The logistic regression model with resampled data (Model 2) is recommended for its improved overall performance, particularly in handling imbalanced data and accurately predicting high-risk loans.
