# 📊 Bayesian Optimization for Discount Effectiveness

This project uses **Bayesian Optimization** to find the optimal **discount rate** that maximizes profit by balancing unit price and adjusted customer demand.

---

## 🧠 Objective

Given a base price and fixed cost per unit, we simulate profit for different discount rates. The Bayesian optimizer searches the best discount between **5% and 30%**.

---

## 🧮 Model Logic

- **Effective Price** = Base Price × (1 − Discount %)
- **Unit Profit** = Effective Price − Cost
- **Adjusted Demand** = Based on how close the discount is to an ideal reference point (18%)
- **Simulated Profit** = Unit Profit × Adjusted Demand

---

## 🔍 Optimization Method

- **Library**: `bayes_opt`
- **Bounds**: Discount ∈ [5%, 30%]
- **Goal**: Maximize simulated profit

---

## ✅ Results
🔍 Best Discount: 5.00%
💰 Expected Profit: $39,900.00
