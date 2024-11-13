# Credit-Card-Fraud_detection
This project aims to build a machine learning model that detects fraudulent credit card transactions, using imbalance learning techniques to handle the high ratio of legitimate to fraudulent transactions. This repository provides code, data handling strategies, and model training scripts to develop an effective fraud detection model.

Table of Contents
Project Overview
Dataset
Modeling Approach
Imbalance Handling Techniques
Evaluation Metrics
Installation
Usage
Results


Project Overview
Credit card fraud is a critical issue in the financial industry. This project develops a machine learning model to classify transactions as fraudulent or legitimate. Given the highly imbalanced nature of the dataset, special techniques are applied to ensure that the model accurately identifies rare fraud cases without being overwhelmed by the majority of non-fraudulent transactions.

Dataset
The project uses the Credit Card Fraud Detection dataset from Kaggle. The dataset contains transactions made by European cardholders in September 2013. It includes 284,807 transactions, of which only 492 (0.17%) are frauds. Each transaction has 30 numerical features and a binary target variable indicating fraud.

Note: Ensure you have the necessary permissions to use this dataset for your projects.

Modeling Approach
Data Preprocessing: Includes scaling numerical features, handling missing values, and splitting the dataset into training and test sets.
Imbalance Learning: Given the imbalance, techniques like SMOTE, undersampling, and cost-sensitive learning are used to improve the model's sensitivity to fraud.
Model Selection: Various models are tested, including:
Logistic Regression with class weights
Random Forest with balanced class sampling
Gradient Boosting algorithms (e.g., XGBoost with class weights)
Anomaly detection models (e.g., Isolation Forest)
Imbalance Handling Techniques
The following techniques are used to address the class imbalance:

Oversampling: SMOTE (Synthetic Minority Over-sampling Technique) is used to synthetically create new instances of the minority (fraud) class.
Undersampling: Random undersampling of the majority (non-fraud) class to balance the dataset.
Cost-Sensitive Learning: Weights are assigned to classes in the model's loss function, giving higher importance to the fraud class.
Ensemble Methods: Models such as Balanced Random Forest and EasyEnsemble, which are tailored to imbalanced data, are applied to improve model performance.
Evaluation Metrics
Due to the dataset's imbalance, evaluation metrics beyond accuracy are used to assess model performance:

Precision, Recall, and F1 Score
Area Under the Precision-Recall Curve (AUC-PR)
Confusion Matrix: Provides insights into false positives and false negatives.

Results
The final model achieved the following metrics:

Precision: ~0.90
Recall: ~0.75
F1 Score: ~0.82
AUC-PR: ~0.88
