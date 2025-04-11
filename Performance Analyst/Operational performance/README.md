# ⚙️ Operational Performance Analyst Project

This project focuses on analyzing and optimizing operational performance in a manufacturing setting. It involves detecting bottlenecks, improving efficiency, reducing downtime, and simulating the impact of process changes on key performance indicators.

---

## 🧠 Key Components

### 🧱 Bottleneck Detection
- Analyzed **average cycle time** and **downtime** across process stages
- Identified slowest and most resource-intensive stages in production

### 📊 Pareto Analysis
- Used **Pareto chart** to highlight the process stages contributing the most to overall downtime
- Focused efforts on top 20% of contributors

### 👷 Operator Efficiency
- Compared **operator efficiency** across different **work shifts** using box plots
- Highlighted variability and potential shift-level training needs

### ⚡ Energy Consumption Analysis
- Evaluated **energy usage by process stage**
- Visualized operational energy intensity to identify optimization areas

### 🧪 Downtime Reduction Simulation
- Simulated a **30% reduction in downtime**
- Calculated impact on average **cycle time**, estimating potential process speed improvements

### 🔔 Real-Time Alerting System
- Flagged potential delays when:
  - Cycle time exceeded 360 seconds
  - Downtime exceeded 20 minutes
- Output structured for real-time dashboarding or monitoring

### 📈 Machine Behavior Clustering
- Applied **KMeans clustering** to group machine performance profiles
- Visualized clusters with **pair plots** based on:
  - Cycle time
  - Downtime
  - Defect rate
  - Efficiency
  - Energy usage

### 📋 Executive Summary
- Highlights:
  - Top bottleneck stage
  - Stages with the most total downtime
  - Shift-wise average operator efficiency
  - Total number of alerts triggered

---

## 📁 Dataset Overview

The dataset includes:

| Column                | Description                                         |
|------------------------|-----------------------------------------------------|
| `timestamp`           | Time of activity recording                          |
| `process_stage`       | Manufacturing stage (e.g., Assembly, Painting)      |
| `machine_id`          | Machine involved in operation                       |
| `shift`               | Shift during which operation occurred               |
| `units_processed`     | Number of units processed                           |
| `cycle_time_sec`      | Time taken per unit cycle (in seconds)              |
| `downtime_min`        | Minutes of downtime in that hour                    |
| `defect_rate`         | Fraction of defective units                         |
| `operator_efficiency` | Efficiency rating of operator                       |
| `energy_consumed_kwh` | Energy consumed during the cycle                    |

---

## 🛠️ Technologies Used

- **Python**: `pandas`, `matplotlib`, `seaborn`, `scikit-learn`
- **Analysis & Modeling**: KMeans, StandardScaler
- **Visualization**: PairPlot, Bar Plots, Box Plots

---

## 📬 Contact

Questions or collaboration?  
📧 **istfais82@yahoo.com**
