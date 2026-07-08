# TruSource Customer Churn Prediction

> Case competition: built a churn prediction model for a telecom client (TruSource) and translated the results into three concrete retention recommendations, backed by a proposed A/B test.

---

## Business Problem

TruSource's core challenge is customer retention. High churn doesn't just cost current revenue — it forfeits future lifetime value and referral opportunities, while raising acquisition costs to replace lost customers. The goal of this analysis was to identify *why* customers were leaving and translate those drivers into actions the business could take.

## Approach

- Explored the retention dataset (`retentiondata_case.csv`) — shape, distributions, missing values, class balance
- Cleaned and feature-engineered the data, then split into training/test sets
- Benchmarked several classification models to predict churn probability, ultimately recommending a **gradient boosting model** for its predictive performance on this dataset
- Cross-checked the most influential variables to ground recommendations in the model, not just intuition

## Key Results & Recommendations

| Driver | Recommendation |
|---|---|
| Low referral activity | Strengthen referral programs with personalized incentives for successful referrals |
| Billing friction (especially electronic check payers) | Reduce billing friction for electronic check customers |
| Short contract terms | Promote long-term contracts to lock in retention |

**Proposed test:** Baseline churn was ~27%. The recommended next step is a randomized A/B test — treatment group receives personalized referral incentives, control group gets the standard experience — measuring reduction in churn rate and new customers acquired via referral.

**Risks flagged:**
- Users referring only for the incentive, inflating signups short-term without improving long-term retention
- Upfront incentive cost outweighing retained-revenue gains if referral-driven customers don't stick

## Limitations

- The model relies on historical data and may not capture future behavioral shifts
- External factors such as competitor promotions or regional outages weren't included
- Some behavioral motivations behind churn can't be observed directly in structured data

## My Contribution

I focused on understanding the data and translating findings into business recommendations rather than just model output. I advocated for the gradient boosting model given the competition's timeframe, since gradient boosting generally offers the strongest predictive performance without heavy tuning overhead.

**Biggest lesson learned:** the importance of checking and cleaning data thoroughly *before* training — and with more time, I'd compare additional model types, tune hyperparameters, and cross-validate which variables are truly most influential rather than relying on a single pass.

---

## Repository Structure

```
msba-portfolio-MichaelChen/
├── churn_prediction_analysis.ipynb   # Data exploration, cleaning, modeling
└── README.md
```

## Tech Stack

`Python` · `pandas` · `NumPy` · `scikit-learn`

## Author

**Michael Chen** — MSBA Candidate, University of Louisville
[GitHub](https://github.com/mc1025)
