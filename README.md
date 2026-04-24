# supply-chain-inventory-analysis
End-to-end supply chain analytics using Python, MySQL and Power BI

## 📌 Project Overview

A complete end-to-end supply chain analytics project built on the **DataCo Smart Supply Chain Dataset** (180,519 rows | 53 columns). The goal was to identify delivery bottlenecks, analyse inventory performance, understand product profitability, and forecast future demand — exactly the kind of analysis that Manufacturing, FMCG, and Logistics companies need from data analysts.

> **"More than 54.83% of all orders are at late delivery risk — this project identifies exactly why and where."**

---

## 🎯 Business Questions Answered

1. What is the overall late delivery rate and which shipping mode causes the most delays?
2. Which markets and regions are the biggest bottlenecks in the supply chain?
3. Which product categories generate the most revenue and profit?
4. What is the demand forecast for the next 6 months?
5. Can we predict whether a delivery will be late before it happens?

---

## 🔑 Key Findings

| Finding | Insight |
|---|---|
| **54.83% late delivery rate** | More than every second order is at risk of being late |
| **First Class = worst performer** | 95.32% late delivery rate — highest of all shipping modes |
| **Standard Class = best performer** | Only 38.07% late rate — most reliable shipping option |
| **LATAM is the largest market** | 51K+ orders — more than Europe |
| **Fishing is top category** | $6.93M in sales — nearly double the next category |
| **Demand forecast** | 5,147 to 5,347 orders predicted per month (Mar–Jul 2018) |
| **ML model accuracy** | Random Forest achieves 97.5% accuracy in predicting late deliveries |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python (pandas, numpy)** | Data cleaning and feature engineering |
| **Python (matplotlib, seaborn)** | Exploratory data analysis and visualisation |
| **Python (statsmodels)** | Holt-Winters time series demand forecasting |
| **Python (scikit-learn)** | Random Forest late delivery prediction model |
| **MySQL + MySQL Workbench** | SQL analysis — bottleneck detection, aggregations |
| **Power BI Desktop** | Interactive 4-page business dashboard |

---

## 🚀 How to Run This Project

### Step 1 — Clone the Repository
```bash
git clone https://github.com/yourusername/supply-chain-analysis.git
cd supply-chain-analysis
```

### Step 2 — Install Python Dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels
```

### Step 3 — Run Data Cleaning
- Open `2_python_cleaning/data_cleaning.ipynb` in Google Colab or Jupyter
- Upload `DataCoSupplyChainDataset.csv`
- Run all cells
- Download `dataco_cleaned.csv`

### Step 4 — Run SQL Analysis
- Import `dataco_cleaned.csv` into MySQL
- Open `3_sql_analysis/supply_chain_analysis.sql` in MySQL Workbench
- Run each query section
- Export results to `results/` folder

### Step 5 — Run EDA
- Open `4_python_eda/eda_visualisation.ipynb`
- Upload `dataco_cleaned.csv`
- Run all cells — 6 charts will be generated

### Step 6 — Run Forecasting & ML
- Open `5_forecasting_ml/forecasting_ml.ipynb`
- Upload `dataco_cleaned.csv`
- Run all cells — forecast CSV and 3 charts generated

### Step 7 — Open Power BI Dashboard
- Open `6_powerbi/supply_chain_dashboard.pbix` in Power BI Desktop
- All 4 pages load automatically with interactive slicers

---

## 📊 Dashboard Pages

| Page | Content |
|---|---|
| **Page 1 — Executive Summary** | KPI cards, delivery status donut, orders by market, monthly sales trend |
| **Page 2 — Delivery Performance** | Late delivery by shipping mode, world map, market vs shipping mode heatmap |
| **Page 3 — Product & Profit** | Sales treemap by category, sales vs profit scatter plot |
| **Page 4 — Demand Forecast** | 6-month demand forecast using Holt-Winters model |

---

## 🗄️ SQL Analysis Sections

| Section | Focus |
|---|---|
| Step 1 | Table exploration — DESCRIBE and sanity checks |
| Step 2 | Basic data sanity check — row count, date range, market distribution |
| Step 3 | Late delivery analysis — overall rate, by market, by shipping mode |
| Step 4 | Bottleneck region identification |
| Step 5 | Product category performance |
| Step 6 | Delivery status breakdown |
| Step 7 | Customer segment analysis |
| Step 8 | Monthly order trend (time series in SQL) |
| Step 9 | Top 10 profitable and bottom 10 loss-making products |
| Step 10 | Saved views for Power BI connection |

---

## 🤖 ML Model Summary

### Demand Forecasting
- **Model:** Holt-Winters Exponential Smoothing
- **Training data:** Jan 2015 — Feb 2018 (38 months)
- **Forecast period:** Mar 2018 — Jul 2018
- **Accuracy:** MAPE ~8%

### Late Delivery Prediction
- **Model:** Random Forest Classifier
- **Features used:** Shipping mode, order quantity, discount rate, market, customer segment, scheduled shipment days
- **Train/Test split:** 80/20
- **Accuracy:** 97.5%
- **Top predictor:** Days for shipment scheduled

---

## 📈 Dataset Information

| Property | Details |
|---|---|
| **Source** | DataCo Smart Supply Chain Dataset — Kaggle |
| **Link** | https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis |
| **Rows** | 180,519 |
| **Original Columns** | 53 |
| **Cleaned Columns** | 48 |
| **Date Range** | January 2015 — February 2018 |
| **Markets** | Europe, LATAM, Pacific Asia, USCA, Africa |

---

## 💡 Skills Demonstrated

`Data Cleaning` `Feature Engineering` `Exploratory Data Analysis`
`SQL Joins` `SQL Window Functions` `SQL CTEs` `MySQL`
`Time Series Forecasting` `Holt-Winters` `SARIMA`
`Random Forest` `Classification` `Model Evaluation`
`pandas` `numpy` `matplotlib` `seaborn` `scikit-learn` `statsmodels`
`Power BI` `DAX Measures` `Interactive Dashboards`
`Supply Chain KPIs` `Inventory Analysis` `Demand Planning`

---
