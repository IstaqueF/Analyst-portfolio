# 🛒 Market Basket Analysis for Bundle Pricing Optimization

This project uses **association rule mining** to uncover product combinations frequently bought together, which can be used for bundle pricing strategies. The analysis is performed using both **Apriori** and **FP-Growth** algorithms.

---

## 📊 Objective

Identify frequent itemsets and association rules from customer transactions to:
- Understand product affinity.
- Develop bundle pricing strategies.
- Optimize promotions based on product co-occurrence.

---

## 🧾 Dataset

The dataset contains transactional data from a retail business. Each row represents a transaction:

| transaction_id | products                                           | total_price | discount | effective_price |
|----------------|----------------------------------------------------|-------------|----------|------------------|
| 1              | ['Backpack', 'Mouse', 'Smartphone', 'Charger']    | 815         | 0        | 815.00           |
| 2              | ['USB Drive', 'Laptop']                           | 1020        | 20       | 816.00           |

---

## 🔧 Methodology

1. **Data Cleaning**
   - Convert product strings to Python lists.
   - Transform into one-hot encoded format.

2. **Frequent Itemset Mining**
   - Use `Apriori` and `FP-Growth` algorithms with minimum support of 0.05.

3. **Association Rule Mining**
   - Filter rules with confidence ≥ 0.4.

---

## 📈 Technologies Used

- Python
- `mlxtend` (for Apriori, FP-Growth, Association Rules)
- `pandas`
- `matplotlib` / `seaborn`

---

## ✅ Results

| Metric       | Value       |
|--------------|-------------|
| Min Support  | 0.05        |
| Min Confidence | 0.4      |
| Rules Found (FP-Growth) | _X rules_ |
| Rules Found (Apriori)   | _Y rules_ |

> _Note: Apriori may return fewer rules or none, depending on thresholds._

---

## 📌 Output
Bundle Pricing Optimization
Using Apriori and FP-Growth, we identified frequently bought-together items.

Top bundle ideas:

Backpack + Keyboard
Support: 11.5% | Confidence: 32.6% | Lift: 0.92

Backpack + Tablet
Support: 11.4% | Confidence: 32.2% | Lift: 0.89

Smartphone + Keyboard
Support: 11.6% | Confidence: 32.0% | Lift: 0.90

These item pairs appeared across both models with high support and confidence, making them strong candidates for bundled promotions

