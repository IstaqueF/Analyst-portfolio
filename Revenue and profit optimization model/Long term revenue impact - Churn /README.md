# 🔄 Churn Prediction using XGBoost

This project uses a real-world customer dataset to build a churn prediction model using **XGBoost**. The objective is to predict whether a customer will churn based on their subscription behavior and discount history.

---

## 📂 Dataset

The dataset includes the following features:

| Feature              | Description                                     |
|----------------------|-------------------------------------------------|
| `subscription_length`| Number of months the customer has subscribed    |
| `monthly_price`      | Price paid per month                            |
| `total_spent`        | Total amount spent over the subscription period |
| `support_tickets`    | Number of customer support interactions         |
| `competitor_price`   | Price offered by a competitor                   |
| `discount_received`  | Discount the customer received                  |
| `churn`              | 1 if customer churned, 0 otherwise              |

---

## ⚙️ Model Used

- **Algorithm**: [XGBoost Classifier](https://xgboost.readthedocs.io/en/stable/)
- **Loss Function**: Log Loss
- **Evaluation Metrics**: Confusion Matrix, Classification Report, ROC AUC

---

## 📊 Model Evaluation

### 🔢 Confusion Matrix
[[886 107] [144 863]]

### 📄 Classification Report

| Metric     | Class 0 (No Churn) | Class 1 (Churn) |
|------------|--------------------|-----------------|
| Precision  | 0.86               | 0.89            |
| Recall     | 0.89               | 0.86            |
| F1-score   | 0.88               | 0.87            |

**Accuracy**: 87%  
**ROC AUC Score**: **0.95** ✅ (Excellent predictive performance)

---

## 📈 Conclusion

- The model effectively identifies churners with high precision and recall.
- ROC AUC score of **0.95** indicates strong discrimination between churn and non-churn customers.
- This model can support retention strategies by identifying high-risk customers.
