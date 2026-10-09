# OIBSIP — Data Analytics — Level 1 — Task 1: EDA on Retail Sales Data

## 📌 Objective
Perform a thorough Exploratory Data Analysis on a retail sales dataset to uncover patterns, customer behaviour trends, and actionable business insights.

## 🛠️ Tech Stack
Python, pandas, matplotlib, seaborn, Jupyter Notebook

## 📁 Files in this folder
| File | Description |
|---|---|
| `retail_sales.csv` | Input dataset — 3,000 retail transactions (Jan 2022–Jun 2024) across 7 categories, 5 regions, and customer demographics |
| `EDA_Retail_Sales.ipynb` | Full, executed Jupyter Notebook containing the complete EDA with all required visualisations |
| `README.md` | This file |

## 📊 What the notebook covers
- Initial inspection: shape, dtypes, null check
- Descriptive statistics for Quantity, UnitPrice, Revenue
- **Time series analysis**: monthly and quarterly revenue trend line/bar charts
- **Customer demographics**: age group and gender distribution
- **Product analysis**: top 10 best-selling products, revenue by category
- **Correlation heatmap** of numeric variables
- **Additional insight**: region × category revenue heatmap (non-obvious pattern)
- Written observations (markdown cells) after every chart
- Conclusion with 3 specific, actionable business recommendations

## 🔑 Key Findings
1. Revenue spikes seasonally in Nov–Dec — plan inventory and promotions around this window.
2. The 26–45 age bracket drives the largest share of purchases.
3. Category performance varies significantly by region, pointing to an opportunity for region-specific merchandising rather than a uniform national strategy.

## ▶️ How to run
```bash
pip install pandas matplotlib seaborn
jupyter notebook EDA_Retail_Sales.ipynb
```

## 🎥 Demo Video
[Add your LinkedIn/demo video link here after recording — 2-second title card: Full Name, Track (Data Analytics), Task Title (EDA on Retail Sales Data)]

---
Submitted as part of the **Oasis Infobyte Summer Internship Program (OIBSIP)** — Data Analytics track.
