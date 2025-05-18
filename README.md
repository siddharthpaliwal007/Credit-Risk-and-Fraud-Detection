# Project Title 
Credit Risk Assessment and Fraud Detection Using Machine Learning

## 1. Background: What is Credit Risk and Fraud Detection?
### Credit Risk:
This is the risk of a borrower defaulting on a loan or credit card repayment. If a bank cannot recover the money, it loses both principal and interest.</br>
- Credit Risk Assessment is about predicting how likely a person or company is to repay a loan.</br>
- Banks want to minimize this risk while still giving credit to worthy borrowers.

### Fraud Detection:
This focuses on identifying suspicious or fake transactions, such as:</br>
- Identity fraud (e.g., fake users)</br>
- Synthetic fraud (real + fake data mix)</br>
- Stolen card usage</br>
- Rapid fire transactions or behavior anomalies

## 2. Problem Statement
Design and deploy Machine Learning models to:</br>
- Predict the probability that a user might default (credit risk).</br>
- Detect fraudulent applications or transactions.

## 3. Dataset Overview
### Source: 
Kaggle - Credit Card Fraud Detection Dataset</br>
### Description: 
This dataset contains transactions made by European cardholders in September 2013. It includes 284,807 transactions, with 492 labeled as fraudulent.</br>
### Features:
- Time: Seconds elapsed between each transaction and the first transaction in the dataset.</br>
- V1 to V28: Result of a PCA transformation to protect confidentiality.</br>
- Amount: Transaction amount.</br>
- Class: Target variable (0 for legitimate, 1 for fraud).

## 4. Steps Involved
### A. Data Collection and Exploration
- Understand variables (numerical/categorical).</br>
- Clean missing values.</br>
- Understand class balance (fraud cases are often <1%).

### B. Feature Engineering
- Transform categorical features (e.g., job type).</br>
- Normalize numeric features (e.g., income, loan amount).</br>
- Create new features (e.g., debt-to-income ratio).

### C. Handling Imbalanced Data
- Fraud cases or defaulters are rare (usually <5%).</br>
- Use SMOTE (Synthetic Minority Over-sampling Technique) or under-sampling to balance data.</br>

### D. Modeling
* Train ML models like:</br>
  - XGBoost (robust to imbalanced data)</br>
  - Random Forest / Decision Trees</br>
  - Logistic Regression (baseline)</br>
* Models predict:</br>
  - Probability of Default → used for credit scoring.</br>
  - Probability of Fraud → flagging for further checks.

### E. Evaluation Metrics
- AUC-ROC Curve: How well model separates risky from safe.</br>
- Precision/Recall: Especially for fraud where false positives are expensive.</br>
- Confusion Matrix: TP, TN, FP, FN analysis.

## 5. Business Outcomes
### For Credit Risk:</br>
- Predict and reject high-risk applicants before loan approval.</br>
- Adjust interest rates based on predicted risk.</br>
- Reduce Non-Performing Assets (NPAs) and increase portfolio profitability.

### For Fraud Detection:</br>
- Real-time alerts for suspicious activity.</br>
- Reduce losses from fraudulent loans or applications.</br>
- Improve compliance and audit tracking.

## 6. Example Use Case
A fintech company wants to grow its lending business without increasing defaults. Your model helps them:</br>
- Approve more loans to safe borrowers.</br>
- Flag applicants who show fraud signals (e.g., inconsistent income history). 
