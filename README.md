# 🚚 Supply Chain / Inventory Optimization Analysis

![Python](https://img.shields.io/badge/Python-3.10-blue)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange)
![PowerBI](https://img.shields.io/badge/PowerBI-Desktop-yellow)
![Status](https://img.shields.io/badge/Status-Completed-green)

> **"More than 54.83% of all orders are at late delivery risk — this project identifies exactly why and where."**

---

## 📓 View Full Notebooks

| Notebook | Link |
|---|---|
| Phase 1 — Data Cleaning |[▶ Open in Colab](https://colab.research.google.com/drive/1akcNkXDP_Kx_QRMYkg_dLDIn-733XM8U?usp=sharing)
| Phase 3 — EDA & Visualisation | [▶ Open in Colab](https://colab.research.google.com/drive/1hs9z17KPfVNm8QBdxmKEYd40tsiYZgSY?usp=sharing)
| Phase 4 — Forecasting & ML | [▶ Open in Colab](https://colab.research.google.com/drive/1mHmjorSksoz5EKq6Rz3MAXhwEzy2KWUv?usp=sharing)

---

## 📌 Project Overview

A complete end-to-end supply chain analytics project built on the **DataCo Smart Supply Chain Dataset** (180,519 rows | 53 columns). The goal was to identify delivery bottlenecks, analyse inventory performance, understand product profitability, and forecast future demand — exactly the kind of analysis that Manufacturing, FMCG, and Logistics companies need from data analysts.

---

## 📂 Data

The raw dataset is available on Kaggle:
[Download DataCo Dataset](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis)

| Property | Details |
|---|---|
| **Rows** | 180,519 |
| **Original Columns** | 53 |
| **Cleaned Columns** | 48 |
| **Date Range** | January 2015 — February 2018 |
| **Markets** | Europe, LATAM, Pacific Asia, USCA, Africa |

> **Note:** The cleaned dataset `dataco_cleaned.csv` is not included
> in this repository due to file size limits.
> To generate it, download the raw dataset from Kaggle and
> run `2_python_cleaning/data_cleaning.ipynb` notebook.

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
| **Recommendation** | Switch high-priority orders from First Class to Standard Class |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python — pandas, numpy** | Data cleaning and feature engineering |
| **Python — matplotlib, seaborn** | Exploratory data analysis and visualisation |
| **Python — statsmodels** | Holt-Winters time series demand forecasting |
| **Python — scikit-learn** | Random Forest late delivery prediction model |
| **MySQL + MySQL Workbench** | SQL analysis — bottleneck detection, aggregations |
| **Power BI Desktop** | Interactive 4-page business dashboard |

---

## 📊 Key Visualisations

### Late Delivery Rate by Shipping Mode
![(https://raw.githubusercontent.com/suchetade2/supply-chain-inventory-analysis/main/4_python_eda/charts/chart1_late_delivery_by_shipping_mode.png)](https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/late_delivery_by_shipping_mode.png)

### Orders and Profit by Market
![([https://raw.githubusercontent.com/suchetade2/supply-chain-inventory-analysis/main/4_python_eda/charts/chart2_orders_profit_by_market.png](https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/orders_profit_by_market.png))](https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/orders_profit_by_market.png)

### Monthly Sales Trend (2015–2018)
![(https://raw.githubusercontent.com/suchetade2/supply-chain-inventory-analysis/main/4_python_eda/charts/chart3_monthly_sales_trend.png)](https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/monthly_sales_trend.png)

### Top 10 Product Categories by Profit
![(https://raw.githubusercontent.com/suchetade2/supply-chain-inventory-analysis/main/4_python_eda/charts/chart4_top10_categories_profit.png)](https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/top10_categories_profit.png)

### Delivery Status Heatmap by Market
![(https://raw.githubusercontent.com/suchetade2/supply-chain-inventory-analysis/main/4_python_eda/charts/chart5_delivery_heatmap_by_market.png)
](https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/delivery_heatmap_by_market.png)

### Demand Forecast — Next 6 Months
![(https://raw.githubusercontent.com/suchetade2/supply-chain-inventory-analysis/main/5_forecasting_ml/charts/chart8_demand_forecast.png)](https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/demand_forecast.png)

### Late Delivery Prediction — Feature Importance
![[(https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/feature_importance_confusion_matrix.png)
---](https://raw.githubusercontent.com/suchetade2/supply-chain-inventory-analysis/main/5_forecasting_ml/charts/chart9_feature_importance_confusion_matrix.png))
](https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/feature_importance_confusion_matrix.png)

---

## 🗄️ SQL Analysis — What Was Done

| Step | Focus |
|---|---|
| Step 1 | Table exploration — structure and sanity checks |
| Step 2 | Basic data sanity check — row count, date range, market distribution |
| Step 3 | Late delivery analysis — overall rate, by market, by shipping mode |
| Step 4 | Bottleneck region identification |
| Step 5 | Product category performance |
| Step 6 | Delivery status breakdown |
| Step 7 | Customer segment analysis |
| Step 8 | Monthly order trend — time series in SQL |
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
- **Train / Test split:** 80/20
- **Accuracy:** 97.5%
- **Top predictor:** Days for shipment scheduled

---

## 📊 Power BI Dashboard Pages

📄 **[View Dashboard PDF](https://github.com/suchetade2/supply-chain-inventory-analysis/blob/main/Supply%20Chain%20Dashboard.pdf)**

| Page | Content |
|---|---|
| **Page 1 — Executive Summary** | KPI cards, delivery status donut, orders by market, monthly sales trend |
| **Page 2 — Delivery Performance** | Late delivery by shipping mode, world map, market vs shipping mode heatmap |
| **Page 3 — Product & Profit** | Sales treemap by category, sales vs profit scatter plot |
| **Page 4 — Demand Forecast** | 6-month demand forecast using Holt-Winters model |

---

## 💡 Skills Demonstrated

`Data Cleaning` `Feature Engineering` `Exploratory Data Analysis`
`SQL Joins` `SQL Window Functions` `SQL CTEs` `MySQL`
`Time Series Forecasting` `Holt-Winters` `Random Forest`
`Classification` `Model Evaluation` `pandas` `numpy`
`matplotlib` `seaborn` `scikit-learn` `statsmodels`
`Power BI` `DAX Measures` `Interactive Dashboards`
`Supply Chain KPIs` `Inventory Analysis` `Demand Planning`

---

## 👤 Author

**Sucheta De**
- 💼 [LinkedIn](www.linkedin.com/in/suchetadeofficial)
- 🐙 [GitHub](https://github.com/suchetade2)

---

> ⭐ If you found this project helpful, please give it a star!
