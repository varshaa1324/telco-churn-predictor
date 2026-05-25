# Telco Customer Churn Predictor

## Problem
Predict which telecom customers will churn using ML

## Approach
- Data: IBM Telco Customer Churn Dataset (7,043 customers)
- Model: Logistic Regression (79% accuracy)
- Explainability: SHAP values per customer
- AI Memos: Claude AI generates business recommendations

## Results
- 79% accuracy on test set
- Identified top churn drivers: Tenure and Monthly Charges
- Generated plain-English retention memos using Claude AI

## Sample AI Generated Retention Memo

**Customer Risk Profile:** 81% churn probability

**Top Risk Factors (SHAP):**
- Tenure Months: 2.130 (toward churn) — very new customer
- Monthly Charges: 1.219 (toward churn) — high monthly fee
- Total Charges: -0.418 (away from churn) — low total so far

**Claude AI Generated Memo:**
This customer presents an 81% churn probability driven 
primarily by a very short tenure — they are in the most 
vulnerable window of the customer lifecycle, before loyalty 
habits have formed. Compounding this, their high monthly 
charges mean they are holding a premium-priced plan against 
minimal accumulated experience. The retention team should 
initiate a proactive outreach call within 48 hours to assess 
satisfaction and explore a short-term bill credit or plan review.

## Tech Stack
Python, Pandas, Scikit-learn, XGBoost, SHAP, Anthropic API
