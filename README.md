
<img width="1397" height="788" alt="image" src="https://github.com/user-attachments/assets/9add3be2-45f1-4702-afc6-73cd3308c110" />
Credit Risk Analysis & Prediction Dashboard

An end-to-end Credit Risk Analytics and Prediction project combining PostgreSQL, Python, Machine Learning, and Power BI to analyze loan default patterns, identify high-risk borrower segments, and quantify potential financial exposure.

📌 Project Overview

Credit risk assessment requires identifying borrowers who are more likely to default while understanding the business factors contributing to that risk.

This project develops an end-to-end analytics pipeline that transforms raw loan applicant data into:

Risk and default-rate analysis
Engineered borrower risk features
Machine learning-based default predictions
Default probability estimates
Financial exposure and expected-loss metrics
An interactive Power BI dashboard for business analysis
Project Workflow

Raw Loan Data → PostgreSQL → Data Cleaning & Feature Engineering → Python ML Models → Default Probability → Power BI → Business Insights

🛠️ Tech Stack
Technology	Purpose
PostgreSQL / pgAdmin4	Data cleaning, transformation and feature engineering
Python	Data preprocessing and machine learning
Pandas	Data manipulation and analysis
Scikit-learn	Model building, preprocessing and evaluation
Random Forest	Classification model
XGBoost	Classification model and hyperparameter tuning
Power BI	Interactive dashboard and business analysis
DAX	Risk and financial metrics
📊 Dataset

The project uses loan applicant data containing information related to:

Applicant demographics
Income
Employment length
Loan amount
Loan grade
Interest rate
Loan intent
Loan-to-income relationship
Loan repayment/default status

Two datasets are included in the repository:

credit_risk_dataset.csv
new_credit_risk_dataset.csv
🔹 1. Data Preparation & Feature Engineering

The raw loan applicant data was prepared using PostgreSQL.

Data Cleaning
Handled missing numerical values using median imputation.
Handled missing categorical values using mode imputation.
Checked data distributions and default rates across different categories.
Feature Engineering

Additional risk-related features were created, including:

Loan-to-Income Ratio
Employment Category
Age Bands
Income Bands
Interest Rate Bands

These features were used to better understand borrower characteristics and their relationship with loan defaults.

🔹 2. Machine Learning

Categorical variables were encoded using OneHotEncoder.

Two classification models were developed:

Random Forest
XGBoost
Model Optimization

Hyperparameters were tuned using GridSearchCV to improve model performance, particularly for identifying default cases.

Model Performance

The project achieved approximately:

93% Accuracy
75% Recall for Defaults after XGBoost tuning

Recall was given particular importance because correctly identifying potential defaulters is critical in a credit-risk setting.

Feature Importance

The strongest predictors identified by the model included:

Loan-to-Income Ratio
Income
Interest Rate
Loan Amount

The trained model can also generate default probabilities for new loan applicants.

🔹 3. Power BI Credit Risk Dashboard

An interactive Power BI dashboard was developed to translate the analytical and ML results into business-oriented insights.

Key Metrics

The dashboard includes metrics such as:

Good Loans %
Default Rate
Predicted Defaults
Total Loan Amount at Risk
Expected Loss
Default Probability
DAX-Based Risk Metrics

The dashboard includes calculations for:

Default Probability
Actual Loss
Expected Loss

Expected Loss is calculated using:

Expected Loss = Exposure × PD × LGD

where:

Exposure = loan exposure
PD = probability of default
LGD = loss given default
Interactive Filters

Users can analyze risk across:

Loan Intent
Loan Grade
Income Range
📈 Key Business Insights

The analysis identified several important credit-risk patterns:

1. Loan Grade

Higher-risk loan grades, particularly F and G, showed substantially higher default rates.

2. Loan Purpose

The highest default rates were observed for:

Debt Consolidation — 29%
Medical — 27%
Home Improvement — 26%
3. Borrower Characteristics

The New Employees (0–2 years) employment category showed a higher default rate of approximately 30%.

4. Financial Risk Factors

The analysis and model identified Loan-to-Income Ratio, Income, Interest Rate and Loan Amount among the strongest predictors of default.

5. Model Comparison

XGBoost provided better recall for default cases after tuning compared with the Random Forest model.

💰 Risk Overview

The Power BI dashboard currently reports:

Metric	Value
Good Loans	78.18%
Default Rate	22%
Predicted Defaults	21.82%
Total Loan Amount at Risk	$77M
Expected Loss	$68.16M

These values are based on the current project dataset and dashboard calculations.

🎯 Business Objective

The objective is not only to predict whether a borrower may default, but also to translate predictions into business-oriented risk insights.

The analysis can help stakeholders:

Identify high-risk borrower segments
Understand major drivers of default
Monitor default trends across loan categories
Quantify potential financial exposure
Support data-driven lending and risk-management decisions
🖥️ Dashboard Preview




📁 Repository Contents
Credit-Risk-Analysis-Prediction-Dashboard/
│
├── credit_risk_dataset.csv
├── new_credit_risk_dataset.csv
├── Loan Defaulters Final.pbix
├── Loan Prediction Sys.html
└── README.md
File Description

credit_risk_dataset.csv
Original loan applicant dataset used for the analysis.

new_credit_risk_dataset.csv
Dataset used for generating predictions for new applicants.

Loan Defaulters Final.pbix
Power BI dashboard containing credit-risk KPIs, visualizations and DAX-based metrics.

Loan Prediction Sys.html
HTML-based prediction interface/output associated with the loan prediction component.

Credit Risk Analysis | SQL | Python | Machine Learning | XGBoost | Random Forest | Power BI | DAX | Business Analytics

This project demonstrates how data can be transformed into risk insights, predictive signals and business-focused decision support through an integrated analytics workflow.
