____________________________________________________________________________________
## Customer Churn Prediction using Machine Learning (Part 2)
# Project Overview
This project focuses on predicting customer churn using Machine Learning techniques. 
It is the second part of an end-to-end data analytics pipeline, where the output of
a previous data analytics project is used as input for predictive modeling.
The goal is to identify customers who are likely to churn so that businesses can 
take proactive retention actions.
____________________________________________________________________________________
## Project Continuity (End-to-End Pipeline)
This project builds on:
# Part 1: Customer Churn Analysis & Data Preparation
In the previous project, I performed:

•	Data Cleaning

•	Exploratory Data Analysis (EDA)

•	Feature Engineering

The final processed dataset was exported as:

## Note: Cleaned_churn_Data.csv
____________________________________________________________________________________
## Complete Workflow

Raw Data 

      ↓
   
Data Cleaning & EDA (Part 1)

      ↓
   
Feature Engineering

      ↓
   
Cleaned_churn_Data.csv

      ↓
   
Machine Learning Modeling (Part 2)

      ↓
   
Churn Prediction
____________________________________________________________________________________
## Business Problem
Customer churn is a major concern for businesses, especially in the banking sector, 
where retaining customers is more cost-effective than acquiring new ones.
This project simulates a real-world banking scenario 
(similar to Lloyds Banking Group use cases).
____________________________________________________________________________________
## Objective
Build a classification model to predict:

•	0 → Customer Retained

•	1 → Customer Churned
____________________________________________________________________________________
## Machine Learning Workflow

# 1. Data Input

•	Dataset used: Cleaned_churn_Data.csv

# 2. Data Preparation

•	Feature and target separation

•	Removal of irrelevant columns

X = df.drop('ChurnStatus', axis=1)

y = df['ChurnStatus']
____________________________________________________________________________________
# 3. Train-Test Split

train_test_split(X, y, test_size=0.2, random_state=42)
____________________________________________________________________________________
# 4. Handling Class Imbalance

Applied SMOTE (Synthetic Minority Oversampling Technique):

from imblearn.over_sampling import SMOTE

smote = SMOTE(random_state=42)

X_train_sm, y_train_sm = smote.fit_resample(X_train, y_train)
_____________________________________________________________________________________
# 5. Model Training

Trained multiple ensemble models:

•	Random Forest

•	XGBoost

•	Gradient Boosting

•	LightGBM
_____________________________________________________________________________________
# 6. Model Evaluation

Models were evaluated using:

•	Accuracy

•	ROC-AUC Score

•	Confusion Matrix

•	Cross-Validation
_____________________________________________________________________________________
## Model Performance

•	Achieved moderate predictive performance

•	Random Forest performed best in terms of accuracy

•	XGBoost showed better class separation (ROC-AUC)

•	Cross-validation indicates stable performance across multiple splits

Note: The model serves as a baseline, with scope for further improvement.
______________________________________________________________________________________
## Key Insights

The most influential features impacting churn:

•	TotalSpent

•	LoginFrequency

•	Age

•	ServiceInteractions

Insight:

Customer engagement and spending behaviour are strong indicators of churn risk.
______________________________________________________________________________________
## Tech Stack

# Programming Language:

•	Python

# Libraries:

•	Pandas

•	NumPy

•	Matplotlib

•	Seaborn

•	Scikit-learn

•	Imbalanced-learn (SMOTE)

# Machine Learning Models:

•	Random Forest

•	XGBoost

•	Gradient Boosting

•	LightGBM
_______________________________________________________________________________________
## Key Learnings

•	Built a complete end-to-end machine learning pipeline

•	Transitioned from Data Analytics → Machine Learning

•	Understood class imbalance handling (SMOTE)

•	Learned how to evaluate models using multiple metrics

•	Identified real-world limitations and improvement areas
_______________________________________________________________________________________
## Conclusion

This project demonstrates how to:

•	Convert prepared data into predictive insights

•	Build a real-world ML solution for churn prediction

•	Understand model performance and limitations
________________________________________________________________________________________
## Connect With Me

If you found this project useful or have feedback:

•	⭐ Star this repository

•	💬 Share your suggestions

•	🤝 Connect with me on LinkedIn
________________________________________________________________________________________
## Project Files

•	Cleaned_churn_Data.csv → Input dataset

•	CUSTOMER CHURN PREDICTION USING MACHINE LEARNING.ipynb → ML implementation

•	README.md → Project documentation
________________________________________________________________________________________
_________________________________________________________________________________________

