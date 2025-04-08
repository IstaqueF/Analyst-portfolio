# 👥 Customer Segmentation using K-Means Clustering

This project applies **K-Means clustering** to segment customers based on behavioral and economic features. It helps identify distinct customer groups for targeted pricing, personalized marketing, and retention strategies.

---

## 📊 Dataset Overview

| Feature               | Description                                             |
|------------------------|---------------------------------------------------------|
| `customer_income`      | Annual income of the customer                           |
| `purchase_frequency`   | Number of purchases per period                          |
| `avg_cart_value`       | Average value of items in the cart                      |
| `discount_sensitivity` | Tendency to respond to discounts (0 to 1 scale)         |
| `loyalty_score`        | Loyalty score based on past purchases and retention     |

---

## 🎯 Objective

- Cluster customers into meaningful segments using unsupervised learning
- Profile each segment for business insights
- Visualize and interpret key patterns (e.g., income vs frequency)

---

## 🔧 Methodology

1. **Preprocessing**:
   - Features scaled using `StandardScaler`
   - Optional log-transform for highly skewed variables

2. **Modeling**:
   - Elbow method used to determine optimal number of clusters
   - Final clustering done with `KMeans (k=4)`

3. **Profiling**:
   - Cluster-wise mean comparison to interpret characteristics

4. **Visualization**:
   - Scatter plot of `customer_income` vs `purchase_frequency` colored by cluster

---

## 🔍 Sample Output

**Optimal Clusters**: 4  
**Silhouette Score**: 0.14
**Davies-Bouldin Index: 1.87
