# Credit Risk Profiling

## Overview
This project analyzes borrower characteristics to identify higher-risk credit profiles using demographic, financial, and loan-related variables. Because the dataset did not include a default or risk target label, a composite risk score was engineered using credit amount, loan duration, and account-related indicators to approximate borrower risk.

## Tools Used
- Python
- Pandas
- Seaborn
- Matplotlib
- Jupyter Notebook

## Project Questions
- Which borrower characteristics are associated with higher-risk profiles?
- How do loan amount and duration vary across risk groups?
- Do housing status and credit purpose show meaningful differences in risk?
- What proportion of borrowers fall into low, medium, and high-risk categories?

## Data Preparation
The dataset included borrower demographic and financial profile information, but no default target variable. Missing values in savings and checking account fields were filled with `"none"` to preserve those records for analysis.

A composite `risk_score` was created using four indicators:
- Credit amount above the dataset median
- Loan duration above the dataset median
- Savings account classified as `little` or `none`
- Checking account classified as `little` or `none`

Borrowers were then grouped into:
- **Low risk**
- **Medium risk**
- **High risk**

## Key Findings
- Higher risk profiles are associated with significantly larger credit amounts
- Nearly half of borrowers (45.7%) fall into the high-risk category
- Customers with free housing show higher average risk scores than those who own or rent
- Discretionary credit purposes, such as vacation/other and business, show higher average risk scores than essential purposes such as repairs or domestic appliances
- The distribution of risk levels suggests the portfolio is skewed toward medium- and high-risk borrower profiles

## Files
- `notebooks/german_credit_analysis.ipynb` — main analysis notebook
- `data/german_credit_data.csv` — source dataset used for profiling

## Summary
This project demonstrates feature engineering, borrower segmentation, and financial risk analysis in the absence of a labeled default variable. It highlights how analysts can still generate meaningful lending insights when working with imperfect real-world data.
