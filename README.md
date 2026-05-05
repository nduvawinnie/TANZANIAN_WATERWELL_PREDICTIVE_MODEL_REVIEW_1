---

## Libraries Used
```python
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split, GridSearchCV
from sklearn.preprocessing import StandardScaler
from sklearn.pipeline import Pipeline
from sklearn.metrics import classification_report, confusion_matrix
```

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

## Contributors
- Winnie Nduva

---

## License
This project is licensed under the MIT License
