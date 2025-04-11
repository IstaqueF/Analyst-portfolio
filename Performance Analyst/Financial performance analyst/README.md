# 💰 Financial Performance Analyst Project

This project analyzes a company's financial performance over time, focusing on profitability trends, forecasting future profits, evaluating return on investment (ROI), and detecting unusual financial behaviors. The aim is to provide decision-makers with key insights for strategic financial planning.

---

## 🧠 Key Components

### 📊 Exploratory Data Analysis
- Review of quarterly performance metrics across departments
- Summary statistics and departmental distribution analysis

### 📈 Profit Trend Visualization
- Line chart of average quarterly profit across the organization
- Clear visual of profit evolution over time

### 🔮 Time Series Forecasting
- Forecasted company-wide profit using **Prophet**
- Projected revenue over the next **4 quarters**
- Model evaluation with **MAPE** and **RMSE** using backtesting

### 🧪 Scenario Simulation
- Simulated a **10% increase in expenses**
- Recalculated profit to evaluate financial risk
- Quantified average profit loss due to rising expenses

### 🚨 Anomaly Detection
- Applied **Isolation Forest** to detect anomalies in expenses
- Flagged and counted outliers for further financial investigation

### 🏢 Department-Wise Profitability
- Compared average profit across departments
- Identified best- and worst-performing business units

### 💹 ROI vs Profit Analysis
- Scatter plot exploring the relationship between **ROI percentage** and **profit**
- Insights on which departments generate high profit with efficient capital use

### 📋 Executive Summary
- Highlights:
  - Top and bottom performing departments
  - Forecasted profit trends and backtest results
  - Impact of expense changes on profitability
  - Anomalies flagged for further review

---

## 📁 Dataset Overview

The dataset includes:

| Column         | Description                                      |
|----------------|--------------------------------------------------|
| `quarter`      | Timestamp of financial quarter                   |
| `department`   | Business unit (e.g., Sales, Marketing)           |
| `revenue`      | Total revenue generated                          |
| `expenses`     | Total operational expenses                       |
| `profit`       | Net profit (revenue - expenses)                  |
| `roi_percentage` | Return on investment as a percentage           |

---

## 🛠️ Technologies Used

- **Python**: `pandas`, `matplotlib`, `seaborn`, `prophet`, `scikit-learn`
- **Forecasting**: Facebook Prophet
- **Anomaly Detection**: Isolation Forest
- **Evaluation Metrics**: MAPE, RMSE

---

## 📬 Contact

For collaboration or questions, feel free to reach out:  
📧 **istfais82@yahoo.com**
