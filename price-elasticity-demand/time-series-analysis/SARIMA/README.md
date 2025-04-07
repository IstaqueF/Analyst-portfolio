# 📊 SARIMA Demand Forecasting

This project demonstrates how to use a **Seasonal ARIMA (SARIMA)** model to forecast product demand based on historical sales and contextual features.

---

## 🧠 What is SARIMA?

SARIMA stands for:
- **Seasonal** AutoRegressive Integrated Moving Average
- Adds **seasonality** components to the regular ARIMA model.
- Model defined as: **SARIMA(p, d, q)(P, D, Q, s)**

Where:
- `p`: AutoRegressive terms
- `d`: Differencing order (for stationarity)
- `q`: Moving average terms
- `P, D, Q`: Same as above, but for seasonal components
- `s`: Seasonal cycle length (e.g. 12 for monthly data)

---

## 📌 Dataset Overview

We use a time series dataset with the following features:

| Column             | Description                          |
|--------------------|--------------------------------------|
| `date`             | Date of observation                  |
| `price`            | Product price                        |
| `demand`           | Units sold (target variable)         |
| `competitor_price` | Price of closest competitor          |
| `economic_index`   | Macro indicator score                |
| `promotion`        | 1 if under promotion, else 0         |
| `day_of_week`      | Day number (1–7)                     |
| `month`, `year`    | Calendar components                  |
| `demand_moving_avg`| Smoothed demand trend                |
| `price_change`     | % change in price from previous day  |
| `demand_lag_1`     | Lagged demand (yesterday’s value)    |

---

## ⚙️ Steps Performed

1. **Stationarity Test (ADF Test)**:
- ADF Statistic: **-1.25**
- p-value: **0.65**
- ❌ **Non-stationary** → Apply differencing

2. **First Differencing**:
- ADF Statistic: **-7.39**
- p-value: **8.07e-11**
- ✅ **Stationary**

3. **Model Identification** (based on ACF/PACF):
   - `(p,d,q) = (1,1,2)`
   - Seasonal terms: `(P,D,Q,s) = (1,1,1,7)`

4. **SARIMA Model Training**:
   - Trained on historical demand

5. **Forecasting**:
   - Forecasts future demand over a test window
   - Includes prediction interval

6. **Evaluation**:
   - RMSE: `27.60`
   - Visual plot showing predicted vs actual demand

---

## 📈 Output Example

```plaintext
ADF Test (Original): p = 0.65 → Not stationary
ADF Test (1st Diff): p = 8.07e-11 → Stationary

Selected SARIMA Order: (1,1,2)(1,1,1,7)

RMSE: 27.60
