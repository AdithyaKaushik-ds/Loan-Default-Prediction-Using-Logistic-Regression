# Loan-Default-Prediction-Using-Logistic-Regression

This project focuses on predicting the likelihood of loan default in the personal loan segment using data from LoanTap. The objective is to optimize the loan underwriting process by accurately classifying applicants based on their repayment capability. A Logistic Regression model was developed with careful data preprocessing, feature engineering, and evaluation.

📌 Problem Statement

LoanTap seeks to automate its credit risk assessment by identifying factors influencing loan repayment. The aim is to:

Predict borrower creditworthiness using loan application data.

Minimize false negatives (i.e., approving defaulters) and false positives (i.e., rejecting good customers).

Improve lending efficiency while managing non-performing assets (NPAs).

📊 Exploratory Data Analysis (EDA)

Target Imbalance: 80% loans are fully paid, 20% are charged-off.

Key Insights:

Most loans are of 36 months term (76%).

Grade ‘B’ is most common and more likely to be fully paid.

59% of loans are for debt consolidation; 21% for credit card repayment.

Features like loan amount, interest rate, and DTI are skewed with significant outliers.

🔧 Data Preprocessing & Feature Engineering

Missing values handled using imputation and domain logic (e.g., grouped mort_acc by total_acc).

Outliers were removed using the 3σ (standard deviation) rule.

Feature Engineering:

Created flags from public records and bankruptcy history.

Extracted zip_code and state from the address.

Applied OneHotEncoding on categorical features.

SMOTE applied to handle class imbalance during model training.

🤖 Model Building & Evaluation

Model: Logistic Regression

Scaling: MinMaxScaler

Train/Test Split: 80/20 with stratified sampling

Performance Metrics:

Test Accuracy: 80%

Test F1 Score: 0.61

Test Recall: 0.81

Test Precision: 0.49

ROC-AUC: 0.91

AUPRC: ~0.78 (Precision-Recall Curve Area)

🧠 Feature Importance

Top impactful features:

zip_code features (strongly correlated with defaults)

dti, open_acc, loan_amnt

Negative impact from annual_inc, application_type_JOINT

🧩 Recommendations

Maximize F1 Score and AUPRC to balance recall and precision.

Use geographical attributes cautiously—they are powerful predictors but may introduce bias.

Explore complex models (e.g., Random Forest) for better nonlinear decision boundaries.

Continuously monitor false positive and false negative trade-offs using threshold tuning.
