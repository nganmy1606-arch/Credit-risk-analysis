# Credit-risk-analysis
EDA and predictive modeling on a credit risk dataset
Overview
This project analyzes a Kaggle credit risk dataset of 32,581 loan applications to identify the borrower and loan characteristics most associated with default, and builds a logistic regression model to support lending decisions. The analysis is structured around the 5C credit risk framework (Character, Capacity, Capital, Collateral, Conditions).

Key Findings
loan_percent_income is the strongest single predictor of default risk, and default rates rise sharply once a loan exceeds ~30% of a borrower's income.
Loan grade and prior default history are strongly linked: lower grades show a much higher proportion of borrowers with a prior default on file.
A baseline logistic regression model achieved 85% accuracy but only caught 52% of actual defaulters, due to class imbalance in the dataset (78% no-default / 22% default).
A rebalanced model improved default recall to 79%, at the cost of precision, a trade-off discussed in the report in terms of the relative business cost of missed defaults vs. false alarms.

Repository Contents
File
Description
Credit_Risk_Analysis.ipynb
Full analysis notebook: data cleaning, EDA, multivariate analysis, feature engineering, and modeling
Credit_Risk_Full_Report.docx
Formal written report with findings, tables, and figures

Methodology
Data Cleaning: removed 165 duplicate rows and 7 rows with logically impossible values (e.g. age of 144); retained legitimate high-income outliers.
Exploratory Data Analysis: distribution analysis, correlation heatmap, and 5C-framework-guided aggregation analysis.
Feature Engineering: log transformation of skewed income data, ordinal/one-hot/binary encoding of categorical variables, multicollinearity resolution, train/test split.
Modeling: baseline and class-balanced logistic regression, compared using precision, recall, and F1-score (not just accuracy, given class imbalance).

Tools Used
Python · pandas · numpy · matplotlib · seaborn · scikit-learn · Google Colab

Dataset Source
Credit Risk Dataset, Kaggle

Author
Ngan
Linkedin: www.linkedin.com/in/anarddoan


