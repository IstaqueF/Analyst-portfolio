# 🧮 Price Prediction using Multiple Linear Regression (MLR)

This project uses a Multiple Linear Regression (MLR) model to forecast **product prices** based on market and promotional factors. It's part of a broader pricing analyst portfolio to demonstrate practical applications of data science in pricing optimization.

---

## 📊 Dataset

The dataset includes:

| Feature            | Description                                           |
|--------------------|-------------------------------------------------------|
| `demand`           | Product demand (units sold)                           |
| `competitor_price` | Competitor's pricing                                  |
| `economic_index`   | Economic sentiment index                              |
| `seasonality`      | Seasonal pattern strength (normalized)                |
| `promotion`        | Promotion flag (0 = No promo, 1 = Promo)              |
| `price`            | **Target** variable to be predicted                   |

---

## 🎯 Objective

To build an MLR model that accurately predicts product prices based on the above features, and evaluate its performance using visual and statistical diagnostics.

---

## 🔧 Methodology

1. Load and explore data
2. Visualize relationships between features
3. Split data into train/test sets
4. Train MLR model using `statsmodels`
5. Evaluate performance with RMSE and R²
6. Plot:
   - Actual vs. Predicted Prices (scatter and line plots)
   - Residuals to assess model fit

---

## 📈 Sample Output
Adjusted R²: 0.89
RMSE on test set: 2.75

Points above the line: Predicted > Actual The model thinks the value is higher than it truly is. 👉 Overestimation
Points below the line: Predicted < Actual The model thinks the value is lower than it actually is. 👉 Underestimation

