# 📣 Marketing Performance Analyst Project

This project evaluates the performance of marketing campaigns, channels, and customer segments to optimize conversions and maximize Return on Advertising Spend (ROAS). It combines feature engineering, predictive modeling, customer segmentation, and budget simulations to generate actionable marketing insights.

---

## 🧠 Key Components

### 🧾 Feature Engineering
- Created key marketing metrics:
  - **CTR (Click-Through Rate)**
  - **CPC (Cost Per Click)**
  - **Conversion Rate**

### 📊 Campaign Performance Analysis
- Visualized **ROAS distribution** across marketing campaigns using boxplots
- Identified high-variance and top-performing campaigns

### 🤖 Conversion Prediction Model
- Built an **XGBoost Classifier** to predict the likelihood of customer conversions
- Model evaluated using:
  - **Classification report**
  - **ROC-AUC Score**
  - **ROC Curve**

### 👥 Customer Segmentation
- Applied **KMeans clustering** on marketing metrics after **PCA** dimensionality reduction
- Identified distinct customer behavior groups for targeting optimization

### 💸 ROI Simulation
- Simulated marketing ROAS under different **budget scenarios**
- Identified the **optimal budget range ($2000–$5000)** for maximizing ROI

### 📋 Executive Summary
- Highlighted:
  - Top-performing campaigns by average ROAS
  - Customer segments with the highest conversion rates
  - ROI trends across budget ranges

---

## 📁 Dataset Overview

The dataset contains:

| Column                     | Description                                        |
|----------------------------|----------------------------------------------------|
| `customer_id`              | Unique customer identifier                         |
| `campaign`                 | Campaign name                                      |
| `channel`                  | Advertising channel (e.g., Search, Display)        |
| `customer_segment`         | Segment classification (e.g., New, Returning)      |
| `budget`                   | Marketing budget allocated                         |
| `clicks`                   | Number of ad clicks                                |
| `impressions`              | Number of ad impressions                           |
| `conversions`              | Conversion indicator (0 or 1)                      |
| `customer_acquisition_cost`| Cost to acquire customer                           |
| `revenue_generated`        | Revenue from the campaign                          |
| `roas`                     | Return on Advertising Spend (revenue / budget)     |

---

## 🛠️ Technologies Used

- **Python**: `pandas`, `numpy`, `scikit-learn`, `xgboost`, `matplotlib`, `seaborn`
- **Modeling**: XGBoost Classifier, KMeans, PCA
- **Evaluation**: ROC Curve, Classification Report
- **Simulation**: Budget-based ROAS estimation

---

## 📬 Contact

Interested in working together or have questions?  
📧 **istfais82@yahoo.com**
