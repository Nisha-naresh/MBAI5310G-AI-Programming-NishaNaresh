# Week Two - End-to-End Machine Learning Pipeline

## Task Overview
This task involves building a complete machine learning pipeline from loading 
raw data to training and evaluating a model. The goal is to predict whether 
a bank customer will churn (leave) or stay using Logistic Regression.

## Files in This Folder
- Assignment_2_Nisha_Naresh.ipynb: main notebook for the task
- bank_customer_churn_prediction_dataset.xls: dataset used for training and testing

## Dataset or Input Source
Dataset: Bank Customer Churn Prediction Dataset
- 387 rows and 13 columns
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
- Model: Logistic Regression
- Evaluation: Accuracy, Classification Report, Confusion Matrix

## Key Results
- The model successfully predicted customer churn using 11 features
- Dataset had 345 customers who stayed and 42 who churned
- Logistic Regression was trained on 80% of the data
- The model performed better at identifying customers who stay
- Class imbalance affected the model's ability to detect churners

## Responsible AI Reflection
- The dataset is imbalanced with only 42 churned customers out of 387
- This could cause the model to be biased towards predicting No Churn
- Customer financial data is sensitive and must be handled with privacy in mind
- The model is not fully interpretable for non-technical stakeholders
- Human review would be needed before using this in a real bank setting
- Techniques like SMOTE could be used in future to balance the dataset

## How to Run or Review
1. Open Assignment_2_Nisha_Naresh.ipynb in Jupyter Notebook or Google Colab
2. Upload the dataset file bank_customer_churn_prediction_dataset.xls
3. Update the file path in Cell 1 to match your local path
4. Run all cells from top to bottom in order
5. Required libraries: pandas, scikit-learn, pathlib
