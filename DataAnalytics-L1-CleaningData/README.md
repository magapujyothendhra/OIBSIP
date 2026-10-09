# OIBSIP — Data Analytics — Level 1 — Task 3: Cleaning Data

## 📌 Objective
Take a deliberately messy customer sales dataset and systematically transform it into a clean, analysis-ready dataset, documenting every cleaning decision made along the way.

## 🛠️ Tech Stack
Python, pandas, numpy, Jupyter Notebook

## 📁 Files in this folder
| File | Description |
|---|---|
| `messy_customer_sales.csv` | The raw, uncleaned input dataset (625 rows) |
| `Cleaning_Data.ipynb` | Full, executed Jupyter Notebook containing the data quality report and every cleaning step |
| `cleaned_customer_sales.csv` | The final cleaned, analysis-ready output dataset (601 rows) |
| `README.md` | This file |

## 🧹 What was wrong with the raw data
- **Missing values** in `Age`, `Rating`, `PurchaseAmount`, and `City` (~6% each).
- **24 duplicate rows**.
- **Inconsistent categorical formatting**: `Gender` had 6+ variants of just two values (`Male`/`male`/`M`, `Female`/`female`/`F`); `City` and `ProductCategory` had inconsistent casing and stray whitespace (`'mumbai '`, `'MUMBAI'`, `' Delhi'`).
- **Wrong data type**: `PurchaseAmount` was stored as text because some values were formatted as currency strings (e.g. `'$1,613.36'`).
- **Mixed date formats** in `JoinDate` (four different string formats).
- **Outliers / impossible values**: ages over 100 or negative, purchase amounts that were negative or implausibly large.

## 🔧 How each issue was resolved
1. **Data quality report** — nulls, duplicates, dtype issues, and value-range anomalies were quantified first, before any changes were made.
2. **Missing data**: `Age` → median (robust to skew), `Rating` → mode (discrete scale), `PurchaseAmount` → median (right-skewed), `City` → explicit `'Unknown'` category (never fabricated).
3. **Type correction**: `PurchaseAmount` currency strings were parsed into numeric floats; `JoinDate` was parsed from four mixed formats into a single `datetime64` column.
4. **Duplicates**: 24 exact duplicate rows were identified and removed (625 → 601 rows).
5. **Standardisation**: `Gender`, `City`, and `ProductCategory` were trimmed and normalised into consistent categories; `Name` whitespace was stripped.
6. **Outlier handling**: `Age` was capped to a realistic 0–100 range; `PurchaseAmount` outliers were detected via the IQR method and capped at the IQR fences (rows were kept, not dropped, to preserve sample size).

## 📊 Before vs. After Summary
| Metric | Before | After |
|---|---|---|
| Row count | 625 | 601 |
| Total null values | 208 | 0 |
| Duplicate rows | 24 | 0 |
| `PurchaseAmount` dtype | mixed (str/float) | `float64` |
| `JoinDate` dtype | `object` (mixed formats) | `datetime64` |
| `Gender` categories | 6 inconsistent variants | 3 standardised (`Male`, `Female`, `Unknown`) |

## ▶️ How to run
```bash
pip install pandas numpy
jupyter notebook Cleaning_Data.ipynb
```

## 🎥 Demo Video
[Add your LinkedIn/demo video link here after recording — remember the 2-second title card: Full Name, Track (Data Analytics), Task Title (Cleaning Data)]

---
Submitted as part of the **Oasis Infobyte Summer Internship Program (OIBSIP)** — Data Analytics track.
