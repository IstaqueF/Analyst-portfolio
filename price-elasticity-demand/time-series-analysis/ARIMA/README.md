# 📊 ARIMA Model for Demand Forecasting

This project demonstrates how to apply the ARIMA (AutoRegressive Integrated Moving Average) model to forecast **product demand** based on historical time series data.

---

## 🗂️ Project Overview

We use a dataset containing features like `price`, `competitor_price`, `economic_index`, and more. The objective is to **forecast demand** using the ARIMA model by analyzing its temporal behavior.

---

## 🔍 Dataset Description

Each row in the dataset represents a single day and contains the following columns:

- `date`: Timestamp
- `price`: Selling price of the product
- `demand`: Number of units sold
- `competitor_price`: Competitor pricing
- `economic_index`: General economic condition indicator
- `promotion`: Binary variable indicating if a promotion was active
- `day_of_week`, `month`, `year`, `quarter`, `week_of_year`: Temporal features
- `demand_moving_avg`: Smoothed demand using a moving average
- `price_change`: Day-over-day price change
- `demand_lag_1`: Previous day's demand (lag feature)

---

## ⚙️ Steps Performed

### 1. 📈 Data Preprocessing
- Converted `date` to datetime format and set it as index.
- Checked for nulls and sorted the time series.

### 2. ✅ Stationarity Check
- Plotted rolling statistics and performed the **Augmented Dickey-Fuller (ADF)** test to check if the demand series is stationary.
- Differencing was applied to remove trend/seasonality if needed.

### 3. 🔄 ACF and PACF
- Plotted the **Autocorrelation Function (ACF)** and **Partial Autocorrelation Function (PACF)** to identify suitable values for:
  - `p`: number of autoregressive terms
  - `d`: degree of differencing
  - `q`: number of moving average terms

### 4. 🔧 Model Training
- Fit the **ARIMA(p, d, q)** model to the demand series.
- Evaluated residuals to validate assumptions.

### 5. 🔮 Forecasting
- Forecasted future demand and visualized results.
- Compared actual vs predicted where applicable.

---

## 🧠 ARIMA Model Theory

- **AR (p)**: Autoregressive part — regression on its own past values.
- **I (d)**: Integrated part — differencing to make the series stationary.
- **MA (q)**: Moving average part — regression on past forecast errors.

A series must be **stationary** for ARIMA to work properly (i.e., constant mean and variance over time).

---

## 🧾 Example Output

ADF Test result
ADF Statistic (original): -1.25  
p-value: 0.6526  
❌ Conclusion: Series is NOT stationary

ADF Statistic (after 1st differencing): -9.79  
p-value: 6.38e-17  
✅ Conclusion: Differenced series is stationary

Selected ARIMA order
Based on ACF/PACF plots:
p = 14  # from PACF  
d = 1   # first differencing  
q = 2   # from ACF

Forecast Results
An ARIMA model was used to predict future demand, which historically ranged between 325 and 475 units. The model achieved an RMSE of 27.60, indicating a moderate prediction error relative to the total range.
This level of accuracy suggests the model captures general demand trends but may struggle with short-term fluctuations. It can still be valuable for high-level planning, inventory management, and identifying overall demand direction.




