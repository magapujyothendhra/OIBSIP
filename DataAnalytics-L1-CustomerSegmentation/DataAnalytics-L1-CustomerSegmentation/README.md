# OIBSIP — Data Analytics — Level 1 — Task 2: Customer Segmentation Analysis

## 📌 Objective
Apply clustering algorithms to segment an e-commerce company's customer base into distinct groups based on purchasing behaviour, enabling targeted marketing strategies.

## 🛠️ Tech Stack
Python, pandas, scikit-learn (KMeans), matplotlib, seaborn, Jupyter Notebook

## 📁 Files in this folder
| File | Description |
|---|---|
| `ecommerce_customers.csv` | Input dataset — 800 customers with Recency, Frequency, Monetary (RFM) values |
| `Customer_Segmentation.ipynb` | Full, executed Jupyter Notebook with the complete RFM clustering analysis |
| `README.md` | This file |

## 📊 What the notebook covers
- Data inspection and descriptive statistics (average purchase value, frequency, recency)
- **Feature selection**: RFM (Recency, Frequency, Monetary) — the industry-standard framework for behavioural segmentation
- **Standardisation** with `StandardScaler` before clustering
- **Elbow Method** to determine the optimal number of clusters (K=4)
- **K-Means clustering** applied and visualised via scatter plots (Recency vs Monetary, Frequency vs Monetary)
- **Cluster profiling**: mean RFM values and customer count per cluster
- Bar chart of customers per cluster
- Full marketing-action interpretation for each segment

## 🔑 Segment Summary
| Segment | Behaviour | Recommended Action |
|---|---|---|
| Champions | Recent, frequent, high spend | Loyalty/VIP program, referral incentives |
| Loyal | Consistent repeat buyers | Upsell/cross-sell campaigns |
| At-Risk | Haven't purchased in a long time | Win-back discount campaigns |
| New/Low-Value | Recently acquired, low activity | Onboarding nudges, second-purchase offers |

## ▶️ How to run
```bash
pip install pandas scikit-learn matplotlib seaborn
jupyter notebook Customer_Segmentation.ipynb
```

## 🎥 Demo Video
[Add your LinkedIn/demo video link here after recording — 2-second title card: Full Name, Track (Data Analytics), Task Title (Customer Segmentation Analysis)]

---
Submitted as part of the **Oasis Infobyte Summer Internship Program (OIBSIP)** — Data Analytics track.
