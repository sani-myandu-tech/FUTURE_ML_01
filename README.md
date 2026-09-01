# 🛒 RetailVision AI – Sales & Demand Forecasting System
### FUTURE_ML_01 | Machine Learning Internship Project

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3-orange?logo=scikit-learn)](https://scikit-learn.org)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)]()
[![License](https://img.shields.io/badge/License-MIT-lightgrey)]()

> **Predicting future retail sales with machine learning — enabling smarter inventory decisions, optimised staffing, and data-driven promotions.**

---

## 📌 Project Overview

This end-to-end machine learning project builds a **Sales & Demand Forecasting System** for a multi-category retail business using 4 years of historical transaction data (2015–2018). The system uses time-series feature engineering and two trained ML models to predict monthly sales and generate a **3-month forward forecast**.

**Business Problem:** Without reliable sales forecasts, retailers over-stock (wasting capital) or under-stock (losing revenue). This system solves both problems.

---

## 🗂️ Repository Structure

```
FUTURE_ML_01/
│
├── 📂 data/
│   ├── raw/                    # Original dataset files
│   └── processed/              # Cleaned, feature-engineered data
│
├── 📂 notebooks/
│   └── sales_forecasting.py    # Full analysis & model notebook
│
├── 📂 images/                  # All generated charts & visualizations
│   ├── 01_monthly_sales_trend.png
│   ├── 02_yearly_growth.png
│   ├── 03_seasonality.png
│   ├── 04_category_sales.png
│   ├── 05_feature_importance.png
│   ├── 06_actual_vs_predicted.png
│   ├── 07_future_forecast.png
│   └── 08_model_comparison.png
│
├── 📂 models/                  # Saved trained model files (.pkl)
│   ├── random_forest_sales_model.pkl
│   └── linear_regression_sales_model.pkl
│
├── 📂 reports/
│   └── business_insights.md    # Non-technical business report
│
├── 📂 src/
│   └── utils.py                # Helper functions (optional)
│
├── requirements.txt
└── README.md
```

---

## 🛠️ Tools & Technologies

| Category | Tools |
|----------|-------|
| **Language** | Python 3.10+ |
| **Data Processing** | pandas, NumPy |
| **Visualisation** | Matplotlib, Seaborn |
| **ML Models** | scikit-learn (LinearRegression, RandomForestRegressor) |
| **Model Persistence** | joblib |
| **Environment** | Jupyter Notebook / VS Code |

---

## 🔄 Project Workflow

```
Raw Data → Cleaning → EDA → Feature Engineering → Train/Test Split
    → Model Training → Evaluation → Future Forecast → Business Report
```

### Steps in Detail:
1. **Data Loading** — 9,994 retail transactions (2015–2018)
2. **Data Cleaning** — Handle nulls, duplicates, negative values, parse dates
3. **EDA** — Sales trends, yearly growth, seasonality, category breakdown
4. **Feature Engineering** — 14 features: time-based, cyclical, lag, and rolling stats
5. **Time-Based Split** — Train on 2015–mid 2018, test on last 6 months
6. **Model Training** — Linear Regression + Random Forest (200 trees)
7. **Evaluation** — MAE, RMSE, R², MAPE comparison
8. **Forecasting** — 3-month forward predictions (Jan–Mar 2019)
9. **Business Insights** — Actionable recommendations from model output

---

## 📊 Model Performance

| Model | MAE | RMSE | R² Score | MAPE |
|-------|-----|------|----------|------|
| Linear Regression | $18,400 | $22,100 | 0.83 | 9.8% |
| **Random Forest ✅** | **$9,200** | **$12,600** | **0.91** | **5.2%** |

**Winner: Random Forest Regressor** — 47% lower error, 91% variance explained.

---

## 🔮 3-Month Sales Forecast

| Month | Predicted Sales |
|-------|----------------|
| January 2019 | ~$142,000 |
| February 2019 | ~$118,000 |
| March 2019 | ~$156,000 |

---

## 📈 Key Visualisations

| Chart | Description |
|-------|------------|
| Monthly Sales Trend | Full 4-year historical trend line |
| Yearly Growth | Bar chart + YoY % growth |
| Seasonality | Average sales by month across all years |
| Category Sales | Revenue breakdown by product category |
| Feature Importance | Top predictors in Random Forest |
| Actual vs Predicted | Model accuracy on test period |
| Future Forecast | Next 3 months predicted sales |
| Model Comparison | Side-by-side MAE, RMSE, R² |

---

## 💡 Key Business Findings

- 📈 **November** is the strongest month (+47% above average) — peak Q4 season
- 📉 **February** is the weakest month — ideal for clearance and training
- 💻 **Technology** drives highest revenue growth despite only 19% of transactions
- 🎯 **Discounts > 20%** correlate with profit erosion — cap at 20%
- 📦 **Early Q3 stocking** (August) is critical to meet Q4 demand safely

---

## 🚀 How to Run This Project

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/FUTURE_ML_01.git
cd FUTURE_ML_01

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the notebook
cd notebooks
python sales_forecasting.py
# or open in Jupyter: jupyter notebook sales_forecasting.ipynb
```

---

## 📋 Requirements

```
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
seaborn>=0.12
scikit-learn>=1.3
joblib>=1.3
```

---

## 💼 Business Value

This system enables RetailVision Retail Co. to:
- **Reduce stockouts** by 30–40% with proactive inventory planning
- **Cut overstock costs** by ordering closer to predicted demand
- **Optimise staffing** — hire seasonally before peak, reduce in off-season
- **Time promotions** to amplify natural demand peaks
- **Forecast annual revenue** for budget planning and investor reporting

---

## 👤 Author

**Lungisani Mnyandu**  
Data Science & ML Internship Candidate  
[LinkedIn](https://linkedin.com/in/yourprofile) | [GitHub](https://github.com/yourusername)

---

## 📜 License

This project is licensed under the MIT License — free to use and adapt with attribution.

---
* Internship Portfolio Project | 2025*

