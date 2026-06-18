
# Week Three - Classification Models and Evaluation Metrics

## Task Overview
This task involves training and comparing two classification models to predict 
whether a bank customer will churn or stay. Both Logistic Regression and SVM 
models were trained and evaluated using multiple metrics including accuracy, 
precision, recall and F1 score.

## Files in This Folder
- Assignment_3_Naresh_Nisha.ipynb: main notebook for the task
- bank_customer_churn_prediction_dataset.xls: dataset used for training and testing

## Dataset or Input Source
Dataset: Bank Customer Churn Prediction Dataset
- 380 rows and 12 columns after cleaning
- Features include Age, Account Balance, Monthly Transactions,
  Satisfaction Score, Customer Service Calls and more
- Target column: Customer_Churned (Yes or No)

## Methods Used
- Data loading using pandas
- Data cleaning: removed duplicates and filled missing values
- Feature encoding: OneHotEncoder for categorical columns
- Feature scaling: StandardScaler for numerical columns
- ColumnTransformer for preprocessing pipeline
- Train/Test split: 80% training, 20% testing
- Model 1: Logistic Regression
- Model 2: Support Vector Machine (SVM)
- Evaluation: Confusion Matrix, Accuracy, Precision, Recall, F1 Score

## Key Results
- Both models were trained and evaluated on the same dataset
- Logistic Regression was better at catching actual churners (higher recall)
- SVM was more precise but missed more churners
- Class imbalance affected both models since only 42 out of 380 customers churned
- Recall was identified as the most important metric for this business problem

## Responsible AI Reflection
- The dataset is imbalanced with very few churn examples which affects both models
- Both models are biased towards predicting No Churn due to the majority class
- False negatives are more dangerous as the bank loses customers without taking action
- Customer financial data is sensitive and must be handled with privacy in mind
- Human review is still needed before acting on any mo
