# OIBSIP — Data Analytics — Level 1 — Task 4: Sentiment Analysis

## 📌 Objective
Build a machine learning model that classifies text sentiment (positive, negative, neutral) to provide insight into customer feedback.

## 🛠️ Tech Stack
Python, pandas, scikit-learn (TF-IDF, Naive Bayes, Logistic Regression), matplotlib, seaborn, Jupyter Notebook

## 📁 Files
| File | Description |
|---|---|
| `product_reviews.csv` | 1,500 labelled product reviews (positive/negative/neutral) |
| `Sentiment_Analysis.ipynb` | Full executed notebook |
| `README.md` | This file |

## 📊 What the notebook covers
- Class distribution check, text preprocessing (lowercase, punctuation/stopword removal)
- TF-IDF feature extraction (with explanation)
- Train/test split, 2 classifiers trained: Naive Bayes + Logistic Regression
- Evaluation: accuracy, precision, recall, F1, confusion matrices, full classification report
- Discussion on why Recall matters most for catching negative feedback
- Top-words-per-sentiment visualisation

## ▶️ How to run
```bash
pip install pandas scikit-learn matplotlib seaborn
jupyter notebook Sentiment_Analysis.ipynb
```

## 🎥 Demo Video
[Add your video link — 2-sec title card: Full Name, Track (Data Analytics), Task Title (Sentiment Analysis)]

---
Submitted as part of the **Oasis Infobyte Summer Internship Program (OIBSIP)** — Data Analytics track.
