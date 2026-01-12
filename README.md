# Customer Churn Prediction

## Dataset Access

The dataset used in this project is the Telco Customer Churn dataset from IBM, available on Kaggle.

Due to licensing considerations, the raw data is not included in this repository.
To reproduce the analysis:

1. Download the dataset from Kaggle
2. Place the CSV file in:
   data/raw/WA_Fn-UseC_-Telco-Customer-Churn.csv

## Project Overview
This project focuses on predicting customer churn for a telecommunications company using supervised machine learning techniques. Customer churn refers to customers discontinuing a service, and accurately identifying at-risk customers enables businesses to implement proactive retention strategies.

The objective of this project is to build, evaluate, and interpret classification models that estimate the probability of customer churn based on demographic information, service usage, and billing characteristics.

---
## Dataset
The analysis uses the \*\*Telco Customer Churn\*\* dataset (IBM), which contains customer-level information including:
* Contract type and tenure
* Service subscriptions
* Monthly and total charges
* Customer churn status (target variable)

The target variable is **Churn**, encoded as:
* 1: Customer churned
* 0: Customer retained
---

## Methodology
The project follows a structured data science workflow:
1\. Exploratory data analysis and data cleaning
2\. Handling missing values and data type inconsistencies
3\. Feature encoding and preparation
4\. Train-test splitting with class stratification
5\. Baseline logistic regression modeling
6\. Feature scaling for numerical stability
7\. Evaluation using appropriate classification metrics
8\. Handling class imbalance via class-weighted learning
9\. Comparison with a tree-based model (Random Forest)

---
## Models and Evaluation
The following models were implemented and compared:
* Logistic Regression (baseline, interpretable)
* Class-weighted Logistic Regression (improved churn recall)
* Random Forest Classifier (nonlinear model)

Given the class imbalance in the dataset, evaluation focused on **ROC-AUC**, **precision**, **recall**, and **F1-score**, rather than accuracy alone.

---

## Key Findings
* Churn prediction is inherently imbalanced, requiring metrics beyond accuracy
* Class weighting significantly improves recall for churners
* Contract type, tenure, and monthly charges are strong predictors of churn
* Tree-based models capture nonlinear relationships but are less interpretable

---
## Business Implications
The results demonstrate how predictive modeling can be used to identify high-risk customers before churn occurs. Prioritizing recall for churners aligns with real-world retention strategies, where the cost of missing a churner is typically higher than contacting a non-churner.

---
## Tools and Libraries
* Python
* pandas, numpy
* scikit-learn
* matplotlib, seaborn

---

## Conclusion
This project demonstrates an end-to-end churn prediction pipeline, emphasizing sound data preparation, appropriate evaluation metrics, and business-oriented interpretation. It reflects a practical and industry-relevant application of supervised machine learning.



