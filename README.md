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

## Sample AI Generated Retention Memos

### Customer #1 — 81% Churn Risk

**SHAP Risk Factors:**
| Factor | Value | Direction |
|---|---|---|
| Tenure Months | 2.130 | toward churn |
| Monthly Charges | 1.219 | toward churn |
| Total Charges | -0.418 | away from churn |

**AI Generated Retention Memo:**
This customer presents an 81% churn probability driven primarily by a very short tenure — they are in the most vulnerable window of the customer lifecycle, before loyalty habits have formed. Compounding this, their high monthly charges mean they are holding a premium-priced plan against minimal accumulated experience. The retention team should initiate a proactive outreach call within 48 hours to assess satisfaction and explore a short-term bill credit or plan review.

---

### Customer #2 — 80% Churn Risk

**SHAP Risk Factors:**
| Factor | Value | Direction |
|---|---|---|
| Tenure Months | 2.130 | toward churn |
| Monthly Charges | 1.132 | toward churn |
| Total Charges | -0.423 | away from churn |

**AI Generated Retention Memo:**
Customer #2 mirrors the same high-risk profile as Customer #1 almost exactly — a very new customer paying high monthly charges, with an 80% churn probability driven by the same early-exit dynamics where loyalty and perceived value have not yet had time to develop. The slightly lower monthly charges SHAP score offers negligible practical difference; this customer is equally exposed to value-driven churn if early expectations go unmet. The retention team should apply the same playbook: a proactive welcome call within 48 hours, a review of whether the current plan is well-matched to actual usage, and close monitoring through the first 60–90 days.

---

### Customer #3 — 78% Churn Risk

**SHAP Risk Factors:**
| Factor | Value | Direction |
|---|---|---|
| Tenure Months | 2.130 | toward churn |
| Monthly Charges | 1.031 | toward churn |
| Total Charges | -0.422 | away from churn |

**AI Generated Retention Memo:**
Customer #3 is the third consecutive customer flagged with the same risk profile — short tenure, high monthly charges, low total spend — and at 78% churn probability represents only a marginal improvement over Customers #1 and #2. The pattern across all three accounts strongly suggests a systemic onboarding problem rather than isolated individual risk: new customers on premium plans are consistently failing to find their footing in the early months. Rather than applying the same individual retention playbook a third time, the retention team should escalate this pattern to leadership for a structural review of the new-customer onboarding experience.

---

### Customer #4 — 76% Churn Risk

**SHAP Risk Factors:**
| Factor | Value | Direction |
|---|---|---|
| Tenure Months | 2.058 | toward churn |
| Monthly Charges | 0.991 | toward churn |
| Total Charges | -0.398 | away from churn |

**AI Generated Retention Memo:**
Customer #4 continues the pattern now seen across four consecutive flagged accounts — new customer, high monthly charges, minimal accumulated spend — and while the 76% churn probability is the lowest of the group, the difference is not meaningful enough to warrant a different level of concern. Four customers sharing near-identical SHAP signatures points clearly to a structural acquisition or onboarding issue. The retention team should treat individual outreach as a short-term stopgap only, and escalate to leadership with all four customer profiles for an urgent audit of how new customers on premium plans are onboarded.

---

### Customer #5 — 76% Churn Risk

**SHAP Risk Factors:**
| Factor | Value | Direction |
|---|---|---|
| Tenure Months | 2.201 | toward churn |
| Monthly Charges | 0.868 | toward churn |
| Total Charges | -0.446 | away from churn |

**AI Generated Retention Memo:**
Customer #5 completes a cluster of five high-risk accounts, all sharing the same core signature — new tenure, elevated monthly charges, low lifetime spend — and at this point the individual memo is almost beside the point. Five consecutive customers with near-identical SHAP profiles and churn probabilities ranging from 76–81% is no longer a retention queue; it is evidence of a broken funnel. The retention team should immediately compile all five cases into a single escalation brief for leadership and push for a cross-functional response involving sales, product, and customer experience.

---

## Key Insight 🔍
All 5 high risk customers share the same pattern:
| Common Factor | Insight |
|---|---|
| Short Tenure | New customers haven't built loyalty yet |
| High Monthly Charges | Premium plans without proven value |
| Low Total Charges | Recently joined, easy to lose |

**This is not 5 individual problems — it is a systemic onboarding issue.**



## Tech Stack
Python, Pandas, Scikit-learn, XGBoost, SHAP, Anthropic API
