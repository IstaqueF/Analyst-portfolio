
# 🔮 Demand Forecasting using Prophet

This project uses **Facebook Prophet**, a powerful additive time series model, to forecast product demand. Prophet is designed to handle seasonality, trends, and holidays effectively with minimal tuning.

---

## 📁 Dataset Overview

The dataset contains the following columns:

- `date`: Daily date index
- `demand`: Target variable to forecast
- Other features: `price`, `competitor_price`, `promotion`, `economic_index`, calendar info like `day_of_week`, `month`, `year`, and engineered features

---

## ⚙️ Why Prophet?

Prophet is useful because:

- It automatically detects **trend** and **seasonality**
- Supports **holidays/special events** with custom regressors
- Requires minimal preprocessing
- Interpretable with built-in plots

Prophet assumes your data contains:
- **`ds`**: Date column  
- **`y`**: Target column (demand in this case)

---

## 🔧 Model Features

We included the following in our Prophet model:

- **Daily trend** with changepoint flexibility
- **Yearly seasonality**
- **Weekly seasonality**
- Custom **regressors** (like `promotion`, `price_change`) to improve accuracy

---

## 📊 Results

- The model captures both **trends** and **seasonal demand cycles**
- Forecast follows expected business patterns
- RMSE is acceptable given daily demand fluctuations
- Prophet provides **uncertainty intervals** to understand forecast confidence

---

## 📈 Output Example

Forecast horizon: 90 days
Future demand shows weak correlation with declining trend
RMSE: 79.27
The model can improved as the RMSE is quite high considering the demand range of 325 - 475
