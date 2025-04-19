# Customer Churn Prediction & CLTV-Based Retention Strategy | Telecom Sector
![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)   
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)  
![NumPy](https://img.shields.io/badge/NumPy-Array%20Computing-013243?logo=numpy&logoColor=white)  
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?logo=matplotlib&logoColor=white)  
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Graphics-2E6E9E?logo=python&logoColor=white)  
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-ML-FF9900?logo=scikitlearn&logoColor=white)  
![XGBoost](https://img.shields.io/badge/XGBoost-Gradient%20Boosting-EC2D01?logo=python&logoColor=white)  

The goal of this project is to analyze churn behavior, identify risk factors, and provide actionable recommendations to improve retention and maximize customer lifetime value (CLTV).

This project evaluates key patterns in churn across different customer cohorts, segments, and behavioral metrics using machine learning classification models (Random Forest & XGBoost), descriptive analytics, and predictive KPIs.

---

## Dataset : https://www.kaggle.com/datasets/alfathterry/telco-customer-churn-11-1-3

---

## Churn Distribution

- **Non-Churned Customers**: 5,174  
- **Churned Customers**: 1,869  
- **Churn Rate**: **26.5%** (moderate imbalance)

> **Loss in CLTV due to churn** = `4238 x 1869` = **$7.9M**

---

## Key Metrics and KPIs

| Metric                        | Insight                                                   |
|------------------------------|------------------------------------------------------------|
| **Churn Rate**               | 26.5% overall – moderate imbalance                         |
| **Average CLTV (Churned)**   | ~$400 lower than non-churned                              |
| **Customer Satisfaction**    | -0.75 correlation with churn (strong negative impact)      |
| **Tenure**                   | -0.35 (new customers churn more)                          |
| **Referrals**                | -0.29 (less engaged users churn more)                     |
| **Total Revenue**            | -0.22 (higher revenue = higher retention)                 |
| **Long Distance Charges**    | -0.22 (value-add bundle worth keeping)                    |

---

## Segment-Based Churn Analysis

### Segment 0:  
- **Profile**: Long-term customers paying ~$29/month  
- **Churn Rate**: 17.5%  
- **Insight**: Retainable via loyalty incentives  
- **Action**: Introduce *“tenure milestones”* perks, upsell premium gradually

### Segment 1:  
- **Profile**: High spenders ($78/month) but **highest churn (46.7%)**  
- **Insight**: High CAC with low CLTV – misaligned plans or dissatisfaction  
- **Action**: Launch *emergency retention offers*, review pricing/value fit

### Segment 2:  
- **Profile**: Top-tier users ($82/month) with **only 14% churn**  
- **Insight**: Most profitable, loyal users  
- **Action**: Shield from price hikes, initiate *referral drives*

---

## Tenure-Based Cohort Insights

| Tenure Group     | Churn Rate | Insight |
|------------------|------------|---------|
| **0–3 Months**   | 56%        | *Critical onboarding failure* – broken first impressions |
| **3–12 Months**  | 38.7%      | Customers don’t perceive long-term value                 |
| **12+ Months**   | 17.1%      | *Healthy retention* from loyal users                     |
| **0–1 Year Cohort** | 47%     | *Price shock post promotions*                            |
| **1–2 Years**    | 28%        | *Product fatigue – falling engagement*                   |
| **2–3 Years**    | 21.6%      | *Proven product value*                                   |
| **3+ Years**     | 11.9%      | *Most stable and profitable segment*                     |

### Retention Recommendations:
- **Onboarding fixes**: Simplify signup, reward first-week success  
- **Check-in offers**: 3-month engagement campaigns  
- **Anniversary upgrades**: 22-month loyalty offers  
- **Referrals + Upsells**: For 3+ year cohort  

---

## Model Performance

###  Random Forest Classifier
```
Precision: 0.95 | Recall: 0.95 | F1 Score: 0.95 | Accuracy: 97%
```

###  XGBoost Classifier (Best)
```
Precision: 0.97 | Recall: 0.95 | F1 Score: 0.96 | Accuracy: 97%
```

- **Recall (Churn Class)**: 95% → *Identifies 19 out of 20 churners*  
- **Precision (XGBoost)**: 97% → *Only 3% false retention offers*  
- **Overall F1 Gain**: 1% over Random Forest  

---

## Feature Importance

Top Predictors:
- **Satisfaction Score** 
- **Churn Score** 
- **Contract Type**  
- **Tenure**  
- **Monthly Charge & Engagement (Referrals, Dependents)**  
- **CLTV and Total Revenue (lower importance)**

---

## Final Recommendations

- **Retention Budget**: Focus on offers <$400 for churners to remain ROI-positive  
- **Segment Focus**:  
  - Grow **Segment 0** with perks  
  - Rescue **Segment 1** with retention campaigns  
  - Protect **Segment 2** and use as a referral engine  
- **Churn Prevention**:  
  - Improve onboarding flow (0–3 month users)  
  - Run mid-tenure re-engagement campaigns  
  - Promote tenure-based rewards  
- **Marketing KPIs to Monitor**:  
  - **Churn Rate by Cohort**  
  - **Customer Lifetime Value (CLTV)**  
  - **Retention Offer ROI**  
  - **Tenure-based Revenue Contribution**  
  - **Precision & Recall of Churn Models**

