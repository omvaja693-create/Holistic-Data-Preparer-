# 🧹 Holistic Data Preparer

### Data Preprocessing & Feature Engineering — Final Project (Red & White Skill Education)

---

## 🎥 Video Explanation

📌 **Google Drive Link:** `https://drive.google.com/file/d/1YZAH9kBGuKGRzhOtkPDdX3pWfpOzSQGe/view?usp=sharing`

> 🎬 5–10 min walkthrough with face + screen recording, covering the full pipeline below.

---

## 📖 Project Overview

This project builds a **complete data preprocessing and feature engineering pipeline** on a synthetic **Customer Credit Risk** dataset (loan default prediction). Raw data is pulled from **four different sources** — CSV, JSON, SQL, and a mock API — merged into one dataset, cleaned, and transformed into an ML-ready format.

🎯 **Goal:** Turn messy, multi-source raw data into a clean, well-engineered dataset ready for a loan-default prediction model.

---

## 🗂️ Data Sources

| Source | Format | Content |
|---|---|---|
| 📄 `main_transactions.csv` | CSV | Core transaction records |
| 🧾 `customer_metadata.json` | JSON | Customer demographic metadata |
| 🗄️ `repayment_history.db` | SQL (SQLite) | Loan repayment history |
| 🌐 Mock API | API | Regional economic indicators |

All four are merged on `customer_id` into a single working dataset.

---

## 🧼 Pipeline Breakdown

### 1️⃣ Data Understanding & Cleaning
- Structure exploration (`.info()`, `.describe()`)
- Custom data quality report (missing %, dtypes, unique counts)
- Duplicate detection

### 2️⃣ Missing Value Handling
- ✅ `SimpleImputer` (median / most-frequent)
- ✅ Manual most-frequent category fill
- ✅ Missing Indicator + Random Sample Imputation
- ✅ `KNNImputer` (multivariate, correlated numeric columns)
- ✅ `IterativeImputer` (MICE algorithm)
- ✅ Complete Case Analysis (evaluated, not used — too much data loss)

### 3️⃣ Outlier Handling
- 📈 Boxplot visualization
- 📊 Z-score method
- 📏 IQR method
- 🎯 Percentile method
- 🧮 Winsorization
- ✂️ Final treatment: domain clipping + IQR-based capping

### 4️⃣ Feature Engineering
- 🕒 Date/time feature extraction (year, month, day, weekday)
- 🔤 Encoding: Ordinal, Label, One-Hot
- 🧩 Numerical encoding: Binning, Binarization, Quantile Binning, K-Means Binning

### 5️⃣ Feature Scaling
- ⚖️ Standardization (Z-score)
- 📐 Normalization
- 🔢 Min-Max Scaling
- 🎚️ MaxAbs Scaling
- 🛡️ Robust Scaling

### 6️⃣ Feature Construction & Transformation
- 🔁 Power Transformer (Box-Cox & Yeo-Johnson)
- 🆕 New features: `debt_to_income_ratio`, `avg_monthly_transactions`

### 7️⃣ Final Deliverable
- 🧾 Drops raw/intermediate columns
- 💾 Exports final ML-ready dataset → `final_cleaned_dataset.csv`

---

## 🛠️ Tech Stack

- 🐍 Python
- 🐼 Pandas / NumPy
- 🤖 Scikit-learn (imputers, encoders, scalers, transformers, KMeans)
- 📉 SciPy (Z-score, Winsorization)
- 📊 Matplotlib
- 🗄️ SQLite3

---

## 📁 Repository Structure

```
Holistic-Data-Preparer/
├── Holistic_Data_Preparer.ipynb    # Main notebook — full pipeline
├── data_set/
│   ├── main_transactions.csv
│   ├── customer_metadata.json
│   └── repayment_history.db
├── final_cleaned_dataset.csv       # Output — ML-ready dataset
├── README.md
└── theory_doc.pdf                  # Conceptual write-up (Part A)
```

---

## ▶️ How to Run

1. Clone the repo 📥
2. Install dependencies: `pandas`, `numpy`, `scikit-learn`, `scipy`, `matplotlib`
3. Update file paths in the data-loading cells to match your local `data_set/` folder
4. Run all cells top to bottom in `Holistic_Data_Preparer.ipynb` ▶️
5. Final dataset saves automatically as `final_cleaned_dataset.csv` ✅

---

## 📋 Submission Checklist

| Deliverable | Status |
|---|---|
| 📓 Jupyter Notebook (practical implementation) | ✅ |
| 📁 GitHub repo (code + README) | ✅ |
| 📄 PDF theory document | ⬜ |
| 🎥 Video walkthrough (face + screen) | ⬜ |

---

## 👤 Author

**Om Vaja**
🎓 AI/ML Student

---

⭐ *Final Project — "Holistic Data Preparer" — Red & White Skill Education*
