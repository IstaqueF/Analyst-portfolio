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

## 📌 Example Output

Apriori Rules:
            antecedents   consequents  support  confidence      lift
0            (Backpack)     (Charger)   0.1124    0.317514  0.902285
1             (Charger)    (Backpack)   0.1124    0.319409  0.902285
2            (Backpack)  (Headphones)   0.1095    0.309322  0.881008
3          (Headphones)    (Backpack)   0.1095    0.311877  0.881008
4            (Backpack)    (Keyboard)   0.1155    0.326271  0.919592
..                  ...           ...      ...         ...       ...
112   (Keyboard, Mouse)      (Laptop)   0.0343    0.309846  0.880996
113  (Keyboard, Laptop)       (Mouse)   0.0343    0.304078  0.872033
114  (Keyboard, Laptop)      (Tablet)   0.0345    0.305851  0.849115
115    (Tablet, Laptop)    (Keyboard)   0.0345    0.305851  0.862038
116    (Monitor, Mouse)      (Laptop)   0.0333    0.301904  0.858413

[117 rows x 5 columns]

FP-Growth Rules:
      antecedents   consequents  support  confidence      lift
0      (Backpack)  (Smartphone)   0.1177    0.332486  0.921269
1    (Smartphone)    (Backpack)   0.1177    0.326129  0.921269
2      (Backpack)      (Tablet)   0.1141    0.322316  0.894826
3        (Tablet)    (Backpack)   0.1141    0.316768  0.894826
4      (Backpack)    (Keyboard)   0.1155    0.326271  0.919592
..            ...           ...      ...         ...       ...
112      (Tablet)  (Smartphone)   0.1163    0.322876  0.894642
113    (Keyboard)      (Tablet)   0.1183    0.333427  0.925673
114      (Tablet)    (Keyboard)   0.1183    0.328429  0.925673
115    (Keyboard)  (Smartphone)   0.1158    0.326381  0.904353
116  (Smartphone)    (Keyboard)   0.1158    0.320865  0.904353

[117 rows x 5 columns]
