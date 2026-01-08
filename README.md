# Emergency Room Wait Time Analysis with Power BI & Machine Learning

![Main Dashboard Overview](/screenshots/Main_Dashboard.png)

## Introduction

Emergency department wait times are a critical operational challenge. Long waits affect patient outcomes, satisfaction, and hospital efficiency, yet the drivers behind delays are often difficult to pinpoint.

This project was built to answer a practical question:

**Where, when, and why do ER wait times break down — and what can hospitals do about it?**

Using historical ER visit data, I developed a complete analytics solution that combines **machine learning predictions**, **model interpretability**, and a **Power BI dashboard** designed for operational decision-making.

---

## Skills Showcased

This project demonstrates end-to-end analytical thinking, from modeling to business storytelling:

- **⚙️ Data Preparation & Feature Engineering (Python)**
  - Cleaned visit-level data and engineered time-based and operational features
  - Structured outputs for downstream BI consumption

- **🤖 Predictive Modeling**
  - Built a Random Forest regression model to predict ER wait times
  - Evaluated performance using MAE and RMSE

- **🔍 Model Interpretability**
  - Impurity-based feature importance to understand internal model behavior
  - Permutation importance to validate real-world feature impact
  - Cross-comparison to confirm which drivers truly matter

- **📊 Power BI & DAX**
  - Created reusable DAX measures for MAE, RMSE, averages, and counts
  - Designed KPI-driven layouts with consistent metric definitions
  - Implemented drillthrough pages for hospital- and hour-level analysis

- **🖱️ Interactive Reporting**
  - Drillthrough navigation for deep-dive analysis
  - Context-aware visuals that respond to user selections
  - Conditional formatting to highlight risk and bias patterns

- **🎨 Dashboard Design**
  - Clean, executive-ready layout
  - Visual hierarchy focused on decision-making
  - Residual analysis to assess prediction quality and bias

---

## Dashboard Overview

### Page 1: Executive Overview

![Executive Overview](/screenshots/Main_Dashboard.png)

This page provides a high-level view of model performance and operational risk.

Key elements include:
- KPI cards showing overall MAE, RMSE, average actual wait, and average predicted wait
- Prediction error by hospital (drillthrough enabled)
- Prediction error across the day to highlight peak-risk hours
- Residual distribution to assess bias and extreme misses
- Feature importance visuals to explain *why* the model behaves the way it does

This page answers:
**Which hospitals and times need attention first?**

---

### Page 2: Hospital Detail (Drillthrough)

![Hospital Drillthrough](/screenshots/Hospital_Drillthrough.png)

This page is accessed by right-clicking a hospital on the main dashboard.

It provides:
- Hospital-specific KPIs (MAE, average waits, visit volume)
- Hourly MAE trend to identify problem periods
- Actual vs predicted wait time comparison by hour
- Residual distribution to detect systematic over- or under-prediction

This page answers:
**What’s happening inside a specific hospital, and when does it struggle most?**

---

### Page 3: Hour Detail (Drillthrough)

![Hour Drillthrough](/screenshots/Hour_Drillthrough.png)

This page is accessed by right-clicking an hour on the main dashboard.

It provides:
- Hour-level KPIs (MAE, RMSE, visit count)
- Hospital performance comparison during the selected hour
- Visit-level table for detailed inspection
- Residual distribution with conditional formatting to flag bias direction

This page answers:
**Which hours are operational pressure points, and which hospitals are most affected?**

---

## Key Insights

- A small number of hospitals consistently contribute disproportionate prediction error
- Evening hours show higher variability, suggesting staffing or demand imbalance
- Time-based and staffing-related features dominate importance rankings
- Most predictions cluster near zero residuals, with a limited number of extreme cases

These insights translate directly into **staffing, scheduling, and triage discussions**.

---

## Repository Structure

```

Healthcare-ER_wait-time-analysis/

>powerbi/
     ER_Wait_Time_Analysis.pbix

>data/
     er_wait_predictions_detailed.csv
     er_wait_by_hospital.csv
     er_wait_by_hour.csv
     
>visuals/
     rf_feature_importances_impurity_top10.png
     rf_feature_importances_perm_top10.png

>screenshots/
     Main_Dashboard.png
     Hospital_Drillthrough.png
     Hout_Drillthrough.png

>README.md

```

## Author

**Tejas Padavalamane**



