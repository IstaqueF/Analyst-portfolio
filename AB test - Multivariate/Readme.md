# 📊 Multivariate A/B Testing with Logistic Regression

This project explores a **Multivariate A/B Test (MVT)** setup where users are shown different combinations of price points, discount levels, and marketing channels. The objective is to identify which combinations drive higher conversion and revenue, and to evaluate the statistical impact of various features on conversion using **logistic regression**.

---

## 📁 Dataset

The dataset contains user-level session data with the following fields:

| Column               | Description                                      |
|----------------------|--------------------------------------------------|
| user_id              | Unique identifier for each user                 |
| price_point          | Price shown to user                             |
| discount_percent     | Discount applied                                |
| marketing_channel    | Source of traffic (email, social, etc.)         |
| device               | Device used during session                      |
| location             | Country of user                                 |
| gender               | Gender of user                                  |
| age                  | Age of user                                     |
| session_duration     | Time spent in session (in seconds)              |
| pages_viewed         | Pages viewed in the session                     |
| conversion           | 1 if purchase made, else 0                      |
| revenue              | Calculated as conversion × price_point          |

---

## 🔍 Objectives

- Evaluate conversion and revenue across different MVT combinations.
- Identify top-performing combinations.
- Fit a logistic regression model to understand the impact of various features on conversion.

---

## 🧪 Methodology

### ✅ 1. Create New Features
- `revenue` column = `conversion × price_point`
- `combo` column = concatenation of price, discount, and channel

### ✅ 2. Grouped Analysis
- Conversion and revenue calculated by `(price, discount, channel)` combinations.
- Top 10 combinations ranked by `revenue_per_user`.

### ✅ 3. Logistic Regression
- One-hot encoded categorical variables:
  - `price_point`, `discount_percent`, `marketing_channel`, `device`, `location`, `gender`
- Target variable: `conversion`
- Evaluated statistical significance of each variable.

---

## 📈 Key Insights

- **Top-performing combo:**  
  `Price: $29.99 | Discount: 5% | Channel: direct`  
  → `Revenue per user = $6.25`, `Conversion rate ≈ 20.8%`

- **Logistic Regression Results:**
  - Most coefficients not statistically significant (`p > 0.05`)
  - Only `price_point_29.99` had a significant negative impact on conversion (`p = 0.002`)
  - Pseudo R-squared = **0.0024** → Model explains very little variance

---
**
## 📉 Logistic Regression Summary (Extract)

| Variable               | Coef     | P-Value  | Significance |
|------------------------|----------|----------|--------------|
| price_point_29.99      | -0.27    | 0.002    | ✅ Significant |
| device_mobile          | 0.015    | 0.823    | ❌            |
| location_UK            | -0.02    | 0.818    | ❌            |
| gender_male            | 0.03     | 0.659    | ❌            |

> ℹ️ Most categorical variables had **no significant impact** on conversion at 95% confidence level.

---**A/B Testing (Multivariate) – Logistic Regression
A logistic regression model was used to evaluate the impact of multiple factors (price points, discounts, channels, devices, and demographics) on conversion probability.

🔍 Key Findings:
The model is statistically not significant overall (LLR p-value = 0.6098, Pseudo R² = 0.0024), meaning it explains very little variation in conversion.

Only price point $29.99 showed a statistically significant effect (p = 0.002), with a negative coefficient (-0.274)—suggesting this price reduces the likelihood of conversion.

All other factors (discounts, marketing channels, device types, etc.) had no significant impact on conversion (p-values > 0.05).

📌 Final Verdict:
This test did not reveal any strong drivers of conversion except that setting the price at $29.99 reduces conversion likelihood. Further testing or alternative modeling may be needed to better understand what influences conversion behavior.



