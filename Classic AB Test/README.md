# 🧪 Classic A/B Testing for Price Optimization

This project evaluates how different price points affect conversion rates and overall revenue using a classic A/B test. It also applies a proportions Z-test to check for statistical significance between price groups.

---

## 📊 Dataset Overview

The dataset contains user interaction data with different prices shown:

| Column         | Description                                 |
|----------------|---------------------------------------------|
| `user_id`      | Unique identifier for each user             |
| `group`        | Group assignment (A or B)                   |
| `price_shown`  | Price presented to the user (£)             |
| `conversion`   | 1 if user converted (made a purchase), else 0 |

---

## 📈 Analysis Workflow

### ✅ 1. Conversion Rate by Price

Grouped users by `price_shown` and calculated:

- Total users
- Total conversions
- Conversion rate per price

| Price (£) | Conversion Rate |
|-----------|-----------------|
| 9.99      | 50.85%          |
| 14.99     | 50.19%          |
| 19.99     | 48.64%          |
| 24.99     | 48.15%          |
| 29.99     | 49.41%          |

### ✅ 2. Visualize Conversion Rate

A simple bar chart was created to show how conversion rate changes with price.

### ✅ 3. Statistical Significance Test

Used a **Z-test for proportions** to compare two price points (e.g., £9.99 vs £29.99):

- **p-value**: 0.360  
  → ❌ Not statistically significant  
  → We fail to reject the null hypothesis (no significant difference in conversion)

### ✅ 4. Revenue Optimization

Calculated **revenue per user** (conversion × price):

| Price (£) | Avg Revenue per User |
|-----------|----------------------|
| 9.99      | £5.08                |
| 14.99     | £7.52                |
| 19.99     | £9.72                |
| 24.99     | £12.03               |
| 29.99     | **£14.82** ✅         |

📌 **Conclusion**:  
Despite slight differences in conversion rate, **£29.99** generates the **highest average revenue per user**.


