# Emergency Room Wait Time Prediction & Analysis

## Project Overview
Emergency department wait times directly impact patient outcomes, satisfaction, and hospital efficiency.  
This project builds an end-to-end analytics solution to **predict ER wait times**, **explain what drives delays**, and **surface operational insights** through an interactive Power BI dashboard.

The focus is not just on building a model, but on turning predictions into **actionable, decision-ready insights** for hospital operations teams.

---
## Objectives
- Predict patient wait times using historical ER visit data
- Identify key drivers of long wait times using model interpretability techniques
- Evaluate model performance across hospitals and time-of-day
- Build a professional Power BI report with drillthrough analysis
- Present insights in a way that supports real operational decisions

---

## Tools & Technologies
- **Python**: pandas, numpy, scikit-learn, matplotlib
- **Machine Learning**: Random Forest Regression
- **Model Interpretability**: Feature importance (impurity-based), permutation importance
- **Visualization & BI**: Power BI, DAX
- **Version Control**: Git, GitHub

---

## Data & Modeling Approach
- Cleaned and prepared ER visit-level data
- Engineered features related to:
  - Hospital characteristics
  - Time of visit (hour, day patterns)
  - Staffing and patient flow indicators
- Trained a Random Forest regression model
- Evaluated performance using MAE and RMSE
- Generated:
  - Row-level predictions with residuals
  - Aggregated summaries by hospital and hour
  - Feature importance outputs for interpretation

---

## Model Interpretability
Two complementary approaches were used:

- **Impurity-based Feature Importance**  
  Shows what the model relies on internally

- **Permutation Importance**  
  Measures how much model performance drops when a feature is shuffled

Agreement between both methods increases confidence in which factors truly matter.

---

## Power BI Dashboard

### Page 1 — Executive Overview
Designed for leadership-level monitoring.

Includes:
- KPI cards: Overall MAE, RMSE, Average Actual Wait, Average Predicted Wait
- Prediction error by hospital (drillthrough enabled)
- Prediction error by hour of day (drillthrough enabled)
- Residual distribution to assess bias and outliers
- Feature importance visuals for transparency

Purpose:
Quickly identify where prediction errors are highest and which factors drive wait times.

---

### Page 2 — Hospital Detail (Drillthrough)
Activated by right-clicking a hospital on the main page.

Includes:
- Hospital-specific KPIs (MAE, average waits, visit count)
- Hourly MAE trend for the selected hospital
- Actual vs predicted wait comparison by hour
- Residual distribution for hospital-level bias analysis

Purpose:
Understand how performance varies within a specific hospital and when delays are most severe.

---

### Page 3 — Hour Detail (Drillthrough)
Activated by right-clicking an hour on the main page.

Includes:
- KPIs for the selected hour (MAE, RMSE, visit volume)
- Hospital performance comparison during that hour
- Detailed visit-level table
- Residual distribution for time-based error patterns

Purpose:
Identify peak-risk hours and operational pressure points.

---

## Key Insights
- Certain hospitals consistently show higher prediction errors, indicating operational variability
- Error spikes during specific evening hours suggest staffing or demand imbalance
- Staffing-related and time-based features consistently rank among the most important drivers
- Residual analysis shows most predictions cluster near zero, with a small number of extreme cases

---

## Repository Structure

Healthcare-ER_wait-time-analysis/
│
├── powerbi/
│ └── ER_Wait_Time_Analysis.pbix
│
├── data/
│ ├── er_wait_predictions_detailed.csv
│ ├── er_wait_by_hospital.csv
│ └── er_wait_by_hour.csv
│
├── visuals/
│ ├── rf_feature_importances_impurity_top20.png
│ └── rf_feature_importances_perm_top20.png
│
├── screenshots/
│ ├── main_dashboard.png
│ ├── hospital_drillthrough.png
│ └── hour_drillthrough.png
│
└── README.md









