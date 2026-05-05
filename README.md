# Tanzanian Water Wells Prediction

## Overview
This project aims to predict the operational status of water points in Tanzania
using machine learning classification models. The project was completed as part 
of a data science project for Water Wells for Africa (WWFA), a non-governmental 
organization committed to ensuring sustainable access to clean water across 
rural and underserved communities in Africa.

---

## Business Problem
Tanzania, a developing nation with a population of over 57 million people, 
faces a critical water access crisis. A significant number of water points 
are either non-functional or in need of repair, leaving millions of citizens 
without reliable access to clean water. This project aims to build a 
predictive classification model that can accurately identify water points 
that are non-functional or in need of repair.

---

## Objectives
1. Identify the key drivers of water point failures in Tanzania
2. Build a predictive classification model to identify functional and 
   non-functional water points
3. Provide actionable insights to guide future water point constructions 
   in Tanzania

---

## Success Metrics
- Successfully identify and rank the top features 
  contributing to water point failure through 
  feature importance analysis and EDA
- Build a predictive classification model with 
  an accuracy of at least 80%
- Successfully provide actionable insights to guide 
  future water point constructions in Tanzania

---
## Data Understanding
- **Source:** Tanzanian Ministry of Water via DrivenData Competition
- **Records:** 59,400
- **Columns:** 40 (31 categorical, 9 numerical)
- **Target Variable:** status_group
  - Functional
  - Non Functional
  - Functional Needs Repair

---

## Data Preparation
- Dropped irrelevant and redundant columns
- Handled missing values using mode imputation
- Treated outliers using capping (Winsorization)
- Feature Engineering:
  - Extracted year and month from date_recorded
  - Created waterpoint_age feature
- One Hot Encoded categorical columns
- Scaled numerical columns using StandardScaler

---

## Models and Results
| Model               | Training Accuracy | Testing Accuracy |
|---------------------|------------------|-----------------|
| Logistic Regression | 73%              | 72%             |
| Decision Tree       | 93%              | 75%             |
| Random Forest       | 93%              | 78%             |

- **Best Model:** Random Forest with a testing accuracy of 78%
- **Target Accuracy:** 80%
- **Pipeline:** StandardScaler + Random Forest

---

## Key Findings
- Gravity is the most common extraction type
- Soft water quality dominates with over 50,000 water points
- Most water points have enough water quantity
- Majority of water points are never paid for
- Pangani basin has the most functional wells
- Lake Victoria basin has the most non-functional wells

---

## Recommendations
1. **Address Class Imbalance** — Use SMOTE to balance the classes
2. **Improve Model Performance** — Explore XGBoost for better accuracy
3. **Focus on High Failure Regions** — Prioritize Dar es Salaam
4. **Improve Management** — Train user groups on water point management
5. **Payment Policy** — Introduce affordable payment scheme
6. **Focus on Water Quality** — Invest in water treatment facilities

---

## Limitations
- Class imbalance made it difficult to identify water points needing repair
- Missing values filled using mode may have introduced bias
- All models did not meet the target accuracy of 80%
- Time constraints limited the number of models explored

---

## Future Work
- Use SMOTE to address class imbalance
- Explore XGBoost and GradientBoosting for better accuracy
- Add more features to improve model performance
- Deploy the model as a web application

---
