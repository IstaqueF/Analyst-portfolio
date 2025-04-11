# 📊 Business Performance Analyst Project

This project provides a comprehensive analysis of business performance across multiple departments and regions using advanced data science techniques. The objective is to uncover key drivers of revenue, forecast future trends, identify operational inefficiencies, and provide actionable insights through visual dashboards and executive summaries.

---

## 🧠 Key Components

### 🔎 Regression Modeling
- **Linear Regression** and **XGBoost Regressor** are trained to predict revenue using operational, marketing, and customer metrics.
- Model performance is evaluated using R² scores.

### 🧬 Feature Importance (SHAP)
- **SHAP** (SHapley Additive exPlanations) is used to interpret the XGBoost model.
- Summary plots highlight the most impactful variables driving revenue.

### 📈 KPI Dashboard
- Department and region-level aggregation of key KPIs:
  - Revenue
  - Sales volume
  - New customers
  - Customer satisfaction
  - Operational cost
  - Marketing spend
- Visualized with bar plots and grouped summaries.

### 📅 Time Series Forecasting
- **Prophet** is used to forecast monthly revenue trends 12 months into the future.
- Trend plots provide a forward-looking view of business performance.

### 🧪 Scenario Simulation
- "What if" analysis performed by simulating a **10% increase in customer satisfaction**.
- Estimated revenue impact is calculated based on trained models.

### 🧩 Clustering for Segmentation
- KMeans clustering applied to performance indicators to segment departments into performance groups.
- Visualized using pair plots for intuitive interpretation.

### 🚨 Anomaly Detection
- **Isolation Forest** identifies unusual data points (e.g., performance anomalies) across business operations.
- Anomalies are flagged and summarized.

### 📋 Executive Summary
- Highlights:
  - Top and bottom performing departments
  - Regional insights
  - Key revenue drivers based on SHAP results

---

## 📁 Dataset Overview

The dataset includes the following columns:

| Column                   | Description                                 |
|--------------------------|---------------------------------------------|
| `date`                  | Monthly timestamp of observation            |
| `department`            | Business unit (e.g., Sales, Marketing)      |
| `region`                | Geographical area (e.g., North, South)      |
| `employees`             | Number of staff                             |
| `operational_cost`      | Monthly operational expenses                |
| `marketing_spend`       | Monthly marketing budget                    |
| `customer_satisfaction` | Satisfaction score (1–5 scale)              |
| `new_customers`         | Count of newly acquired customers           |
| `customer_retention_rate` | Percentage of customers retained         |
| `sales_volume`          | Units sold                                  |
| `revenue`               | Total revenue generated                     |

---

## 🛠️ Technologies Used

- **Python**: pandas, scikit-learn, xgboost, shap, prophet, matplotlib, seaborn
- **Modeling**: Linear Regression, XGBoost, Prophet, KMeans, Isolation Forest
- **Visualization**: Matplotlib, Seaborn
- **Explainability**: SHAP

---

## 📬 Contact

Feel free to reach out for collaboration or feedback:  
📧 **istfais82@yahoo.com**

---

