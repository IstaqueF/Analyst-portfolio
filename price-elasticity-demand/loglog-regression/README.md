# Log-Log Regression: Estimating Price Elasticity of Demand

## 📌 Project Summary

This project demonstrates how to estimate **price elasticity of demand** using a **log-log regression model**. We explore the relationship between demand and price, competitor pricing, and seasonal effects using a dataset of sales data.

---

## 🧪 Dataset

The dataset includes the following columns:

- `price`: The product price
- `demand`: Quantity sold
- `competitor_price`: Price of similar product from competitor
- `seasonality_effect`: Seasonal factors affecting demand

---

## ⚙️ Methodology

1. **Log Transformation**: We log-transform the `price` and `demand` variables to linearize the elasticity relationship.
2. **OLS Regression**: Using statsmodels' OLS to estimate coefficients.
3. **Interpretation**: The coefficient of `log(price)` gives us the **price elasticity of demand**.
4. **Model Summary**: The final output includes R-squared, coefficients, p-values, etc.

---

## 📈 Output Example

```plaintext
Price Elasticity Coefficient: -1.45
Interpretation: A 1% increase in price leads to a 1.45% drop in demand.
