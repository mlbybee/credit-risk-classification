# Module 20 Report - Loan Risk Analysis
# Credit-Risk-Classification Challenge

## Overview of the Analysis:

In this analysis, I aimed to build and evaluate a supervised machine learning models to predict the creditworthiness of borrowers based on historical lending activity data. The primary objective was to classify loans as either healthy (class 0) or high-risk (class 1). Use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Financial Information and Prediction Objective:
The dataset consisted of financial information related to loans, including details such as loan amount, borrower income, debt-to-income ratio, credit score, and other relevant metrics. 

The target variable, loan_status, was a binary classification:
* 0 for healthy loans
* 1 for high-risk loans

## Variable Analysis:
The target variable distribution was analyzed using the value_counts() function, revealing class imbalances that were considered when training models.

## Machine Learning Process Stages: 
1) Data Preparation

* Loaded the dataset (lending_data.csv) into a Pandas DataFrame.
* Separated the feature variables (X) from the target variable (loan_status).
* Split the data into training and testing sets using train_test_split.

2) Model Training and Evaluation

* Built a Logistic Regression model as a baseline classifier.
* Trained the model using the training dataset.
* Made predictions on the test dataset.
* Evaluated model performance using accuracy, precision, recall, and a confusion matrix.

## Methods Used:
* train_test_split
* Logistic Regression
* Confusion Matrix
* Machine Learning Model

## Results: 

Logistic Regression Model: 

* Accuracy Score (f1): 99%
  
    ** Correctly classifies in 99% of the instances
  
* Precision Score:
  
    ** Healthey Loan (class 0): 100%
    ** High-Risk Loan (class 1): 84%
  
* Recall Score:
  
    ** Healthey Loan (class 0): 99%
    ** High-Risk Loan (class 1): 94%

![Classification Report]((https://github.com/mlbybee/credit-risk-classification/blob/main/Resources/classification_report.png)

Confusion Matrix: 
* True Negative: 18,658
* False Negative: 37
* False Positive: 107
* True Positive: 582

![Confusion Matrix]()

## Summary:

Best Performing Model = 

The logistic regression model provided a balanced trade-off between precision and recall. Given the dataset's class imbalance within the datasets, the model's performance was assessed based on whether it prioritized minimizing false negatives (misclassifying high-risk loans as healthy) or false positives (misclassifying healthy loans as high-risk). After assessing the confusion matrix, it successfully performed this analysis. 

Recommendation = 

If minimizing false negatives is crucial (avoiding high-risk loans being approved), a model with higher recall should be prioritized.

If minimizing false positives is important (ensuring eligible borrowers are not unfairly rejected), a model with higher precision is preferred.

Overall, logistic regression provided a solid baseline model for credit risk assessment. 
