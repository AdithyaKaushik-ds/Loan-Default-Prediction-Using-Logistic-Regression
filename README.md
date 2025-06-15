# Loan-Default-Prediction-Using-Logistic-Regression

This project focuses on predicting the likelihood of loan default in the personal loan segment using a real-world lending dataset. The goal is to enhance the credit risk assessment pipeline by classifying loan applicants based on their repayment behavior. A Logistic Regression model is built through systematic preprocessing, feature engineering, and performance evaluation.

📌 Problem Statement

The objective is to build a classification model that identifies borrowers with a high risk of default. By leveraging historical loan data, the model aims to:

Predict creditworthiness using demographic, financial, and behavioral attributes.

Reduce false negatives (approving defaulters) and false positives (rejecting creditworthy applicants).

Support risk-informed lending decisions to minimize non-performing loans.

📊 Exploratory Data Analysis (EDA)

Target Variable: Highly imbalanced with ~80% of loans fully paid.

Key Observations:

Most loans are issued with a 36-month term.

Applicants with grade ‘B’ show better repayment history.

Debt consolidation and credit card payments are the primary loan purposes.

Multiple features show skewed distributions and the presence of outliers.

🔧 Data Preprocessing & Feature Engineering

Missing Values: Addressed using conditional imputation and logical grouping strategies.

Outliers: Handled using the standard deviation method to retain model stability.

Engineered Features:

Extracted ZIP codes and state identifiers from address fields.

Created binary flags from bankruptcy and credit record attributes.

Applied One-Hot Encoding for categorical variables.

Class Imbalance: Addressed using SMOTE to upsample the minority class.

🤖 Model Building & Evaluation

Algorithm: Logistic Regression

Scaler: MinMaxScaler for feature normalization

Split: 80/20 train-test stratification

Results:

Test Accuracy: 80%

F1 Score: 0.61

Recall: 0.81

Precision: 0.49

ROC-AUC: 0.91

AUPRC: ~0.78

🧠 Feature Importance

Geographical ZIP codes had the highest model impact.

Other influential features included DTI, loan amount, and number of open accounts.

Features like annual income and joint application status showed negative coefficients.

🧩 Recommendations

Optimize the F1 Score and AUPRC to balance business risk and opportunity.

Consider enhancing the model using tree-based classifiers for non-linear decision boundaries.

ZIP code-based predictions should be validated to avoid regional bias.

Implement threshold tuning to manage false positives and false negatives.

