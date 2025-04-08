# 💡 Revenue & Profit Optimization Using Polynomial Regression

This project uses **Polynomial Regression** to identify optimal price points that **maximize revenue** and **maximize profit**. It simulates different pricing scenarios based on a real-world dataset of products and models the non-linear relationship between demand, price, and production variables.

---

## 📂 Dataset Description

The dataset contains 10,000 product entries with the following columns:

| Column               | Description                                  |
|----------------------|----------------------------------------------|
| `price`              | Selling price of the product                 |
| `demand`             | Quantity demanded                            |
| `cost_per_unit`      | Cost to produce one unit                     |
| `production_capacity`| Number of units that can be produced         |
| `revenue`            | Calculated as `price × demand`              |
| `profit`             | Calculated as `(price - cost_per_unit) × demand` |

---

## 🎯 Objective

- Model product demand using **polynomial regression** with multiple features
- Simulate how changes in price affect **demand**, **revenue**, and **profit**
- Identify the **price point** that yields:
  - Maximum revenue
  - Maximum profit

---

## 🔍 Methodology

1. **Feature Engineering**  
   Selected input features:
   - `price`
   - `cost_per_unit`
   - `production_capacity`

2. **Model Training**  
   - Applied `PolynomialFeatures(degree=2)`
   - Fitted a `LinearRegression` model on the transformed features

3. **Simulation**  
   - Generated a range of prices (200 values from min to max)
   - Predicted demand at each price
   - Computed revenue and profit for each scenario

4. **Optimal Results**
Best Price for Max Revenue: $499.86 ➤ Maximum Revenue: $21,814.65
Best Price for Max Profit: $499.86 ➤ Maximum Profit: $15,201.07
