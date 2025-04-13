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
This model estimates how various external and internal factors influence product pricing through a multiple linear regression framework. The high R² value of 0.9965 indicates that the model explains nearly all the variance in price, showing strong predictive performance.

Key insights from feature coefficients:

Promotion (-4.03) has the largest negative impact, suggesting that when promotions are active, the price drops significantly—consistent with typical marketing strategies.

Seasonality (+3.00) and Economic Index (+2.09) positively influence price, indicating that prices tend to rise during peak seasonal periods or favorable economic conditions.

Competitor Price (-0.30) has a moderate inverse relationship with our price, suggesting competitive pricing pressure.

Demand (+0.05) shows a small but positive influence, implying slight price flexibility with increased demand.

This model helps interpret price elasticity by quantifying how sensitive price is to changes in other variables, supporting strategic pricing decisions.

