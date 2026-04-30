# global-economic-crisis-risk-prediction
End-to-end ML project predicting economic crisis risk across 47 countries (2000–2035) using inflation, debt, forex reserves &amp; conflict indicators. Random Forest ROC-AUC: 0.97

# 🌍 Global Economic Crisis Risk Prediction & Country Downfall Analysis (2000–2035)

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Google%20Colab-Notebook-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

**Capstone Project 4 (Task 4) · SyntecxHub Data Science Internship · April 2026**

[📊 View Dashboard](#visualizations) · [📓 Open Notebook](#how-to-run) · [📄 Read Report](#deliverables) · [🔍 Explore Dataset](#dataset)

</div>

---

## 📌 Project Overview

This end-to-end data science project analyzes **47 countries across 36 years (2000–2035)** to predict economic crisis risk using macroeconomic, financial, and geopolitical indicators. The project covers historical collapse detection, present-day risk assessment, and future downfall forecasting — delivering actionable intelligence for policymakers, analysts, and financial institutions.

> **"Economic collapse is not sudden — it is the culmination of compounding, predictable vulnerabilities."**

| Metric | Value |
|---|---|
| 🗂️ Dataset Size | 1,692 records × 37 features |
| 🌐 Countries Analyzed | 47 across 6 global regions |
| 📅 Time Horizon | 2000 – 2035 (10-year forecast included) |
| 🤖 Best ML Model | Random Forest — ROC-AUC: **0.97** |
| 🔑 Top Collapse Driver | Sovereign Default Risk Score (r = 0.82) |
| 📈 Future Growth Leader | India (7.3% projected GDP growth) |

---

## 🎯 Project Objectives

- 🔴 **Identify** historically collapsed countries based on economic indicators
- 🟠 **Detect** currently high-risk nations using 2020–2025 data
- 🟡 **Predict** future economic downfall countries (2026–2035)
- 🟢 **Identify** future strong economies based on growth projections
- 🔵 **Explain** root causes of economic decline via correlation analysis
- 🟣 **Recommend** evidence-based recovery solutions
- ⚙️ **Build** ML classifiers to flag high-risk country observations

---

## 📁 Repository Structure

```
global-economic-crisis-risk-prediction/
│
├── 📂 data/
│   └── cleaned_global_economic_crisis_dataset.csv      # Cleaned, feature-engineered dataset
│
├── 📂 notebooks/
│   └── Syntecxhub_GLOBAL_ECONOMIC_CRISIS.ipynb         # Full EDA + ML pipeline (Google Colab)
│
├── 📂 reports/
│   └── Syntecxhub_Global_Economic_Crisis_Project_Report.pdf   # Full project report
│
├── 📂 presentation/
│   └── Global-Economic-Crisis-Analysis.pptx            # PowerPoint slide deck
│
├── 📂 dashboard/
│   └── Syntecxhub_global_economic_crisis_dashboard.html # Interactive HTML dashboard
│
├── 📂 visualizations/
│   ├── viz1_top10_highest_risk_countries.png
│   ├── viz2_inflation_trends_crisis_countries.png
│   ├── viz3_debt_vs_forex_bubble_chart.png
│   ├── viz4_future_economic_forecast.png
│   ├── viz5_currency_devaluation_heatmap.png
│   ├── viz6_conflict_impact_analysis.png
│   ├── viz7_drivers_of_economic_collapse.png
│   └── viz8_ml_roc_curves_feature_importance.png
│
└── README.md
```

---

## 📊 Dataset

**File:** `data/cleaned_global_economic_crisis_dataset.csv`

The dataset contains macroeconomic, financial, and geopolitical indicators for 47 countries spanning 2000–2035. The final 10 years (2026–2035) are model-based projections.

### Key Features

| Category | Features |
|---|---|
| **Macroeconomic** | GDP Growth Rate, Inflation Rate, Unemployment Rate, Poverty Rate |
| **Debt & Fiscal** | External Debt to GDP %, Sovereign Default Risk Score, Money Supply Growth |
| **Financial** | Forex Reserves (USD Billion), Currency Devaluation %, Tourism Revenue Loss % |
| **Geopolitical** | Political Instability Score, War/Conflict Flag, Policy Intervention Flag |
| **Engineered** | Composite Risk Score, High Risk Flag, Debt-to-Forex Ratio, Economic Status |

### Missing Value Treatment

| Column | % Missing | Strategy |
|---|---|---|
| GDP Growth Rate | 2.95% | Country-level median → global median |
| Forex Reserves | 48.9% | Country-level median |
| Poverty Rate | 5.79% | Income-group median |
| Tourism Revenue Loss | 3.90% | Zero-filled (no event = no loss) |

---

## 🔍 Exploratory Data Analysis

**10 Key EDA Questions Answered:**

1. **Which countries have the highest historical economic collapse probability?**
   → Venezuela (99%), Lebanon (98.2%), Zimbabwe (97.8%), Sri Lanka (97.0%)

2. **What are the dominant regions for current high-risk classification (2020–2025)?**
   → Americas (71.2%) and Africa (68.7%) lead in high-risk rates

3. **Which macroeconomic indicators most strongly correlate with economic collapse?**
   → Sovereign Default Risk (r=0.82), Political Instability (r=0.68), Inflation Rate (r=0.61)

4. **How does inflation trajectory precede crisis events?**
   → All top-5 collapse countries showed inflation breaching 20% 1–3 years before peak crisis

5. **What is the structural relationship between external debt and forex reserves?**
   → Countries with Debt-to-Forex ratio > 50 show 3× higher sovereign default probability

6. **Which countries are projected as future strong economies (2026–2035)?**
   → India (7.3%), China (7.1%), Bangladesh (6.6%), Philippines (5.5%)

7. **What is the impact of active war/conflict on collapse probability?**
   → Conflict countries show median collapse probability significantly above non-conflict peers

8. **How does currency devaluation vary by region and decade?**
   → Venezuela and Lebanon show extreme devaluation in 2010s–2020s; European economies near zero

9. **What is the distribution of economic status labels across the dataset?**
   → In Crisis (53.8%), Moderate (33.1%), Strong (8.1%), Contracting (5.0%)

10. **Which income-level groups are most vulnerable to crisis classification?**
    → Low and Lower-Middle income nations show disproportionately higher crisis frequencies

---

## 🤖 Machine Learning Models

**Target Variable:** `High_Risk_Flag` (1 = High Risk, 0 = Not High Risk)

**Preprocessing:** IQR-based outlier capping · Class weight balancing · 80/20 stratified split · 15 numeric features

### Model Performance Comparison

| Model | Accuracy | ROC-AUC | Precision | Recall |
|---|---|---|---|---|
| Logistic Regression | ~0.85 | ~0.91 | ~0.87 | ~0.89 |
| Decision Tree | ~0.87 | ~0.89 | ~0.88 | ~0.91 |
| **Random Forest** ⭐ | **~0.93** | **~0.97** | **~0.94** | **~0.95** |

### Top Feature Importances (Random Forest)

```
Sovereign Default Risk Score     ████████████████████  #1
Economic Collapse Probability    ██████████████████    #2
Political Instability Score      ████████████████      #3
Inflation Rate                   ██████████████        #4
Currency Devaluation %           ████████████          #5
Unemployment Rate                ██████████            #6
External Debt to GDP             ████████              #7
```

---

## 📈 Visualizations

| # | Chart Title | Type | Key Insight |
|---|---|---|---|
| 1 | Top 10 Highest-Risk Countries | Horizontal Bar | Venezuela, Lebanon lead at 99%+ |
| 2 | Inflation Trends – Crisis Countries | Multi-line Time Series | Inflation surges precede collapse |
| 3 | External Debt vs. Forex Reserves | Bubble Chart (log scale) | High debt + low reserves = crisis |
| 4 | Future Economic Forecast 2026–2035 | Dual Panel Bar | Risk vs. growth landscape ahead |
| 5 | Currency Devaluation Heatmap | Heatmap | Venezuela/Lebanon outliers |
| 6 | Conflict Impact Analysis | Boxplot + Bar | War dramatically elevates risk |
| 7 | Drivers of Economic Collapse | Correlation Bar | Default risk dominates |
| 8 | ML ROC Curves & Feature Importance | Dual Panel | RF AUC = 0.97 |

---

## 💡 Key Insights & Recommendations

### Insight 1 — Hyperinflation: The #1 Observable Predictor
Countries with inflation >20% showed collapse probability >85%. Correlation: r = 0.61.

**Recommendations:** Independent central bank mandates · IMF Extended Fund Facility engagement · 12-month forex buffer maintenance

### Insight 2 — High Debt + Low Forex = Structural Crisis Trigger
Debt-to-Forex ratio > 50 → 3× higher default probability. Venezuela (287% debt/GDP), Lebanon (172%), Greece (215%) all lost forex cushions before collapse.

**Recommendations:** Maintain 6-month import cover in reserves · Paris Club debt restructuring · Export base diversification

### Insight 3 — Political Instability Amplifies Everything
Second strongest driver at r = 0.68. War-affected nations (Afghanistan, Ukraine) show near-99% collapse probability regardless of economic policies.

**Recommendations:** Peacekeeping precedes economic reform · Governance reform as aid prerequisite · Institution-building alongside infrastructure

---

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
```
1. Upload cleaned_global_economic_crisis_dataset.csv to your Colab session
2. Open notebooks/Syntecxhub_GLOBAL_ECONOMIC_CRISIS.ipynb in Google Colab
3. Run All Cells (Runtime → Run all)
```

### Option 2: Local Jupyter
```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/global-economic-crisis-risk-prediction.git
cd global-economic-crisis-risk-prediction

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn plotly

# Launch notebook
jupyter notebook notebooks/Syntecxhub_GLOBAL_ECONOMIC_CRISIS.ipynb
```

### Option 3: Interactive Dashboard
```
Open dashboard/Syntecxhub_global_economic_crisis_dashboard.html in any modern browser
No installation required — fully self-contained HTML file
```

---

## 📦 Deliverables

| Deliverable | File | Status |
|---|---|---|
| Cleaned Dataset | `data/cleaned_global_economic_crisis_dataset.csv` |  Complete |
| EDA & ML Notebook | `notebooks/Syntecxhub_GLOBAL_ECONOMIC_CRISIS.ipynb` |  Complete |
| Project Report (PDF) | `reports/Syntecxhub_Global_Economic_Crisis_Project_Report.pdf` |  Complete |
| Interactive Dashboard | `dashboard/Syntecxhub_global_economic_crisis_dashboard.html` |  Complete |
| PowerPoint Presentation | `presentation/Global-Economic-Crisis-Analysis.pptx` |  Complete |
| Visualizations (8 charts) | `visualizations/viz1_*.png → viz8_*.png` |  Complete |

---

## 🔭 Future Scope

-  **Real-time data integration** via World Bank and IMF APIs for live risk monitoring
-  **Deep learning models** (LSTM) for time-series crisis forecasting
-  **NLP sentiment layer** using news headlines and political event feeds
-  **Geospatial risk maps** with country-level choropleth visualization
-  **Interactive web app** (Streamlit / Dash) for live country risk scoring
-  **Ensemble stacking** combining RF, XGBoost, and Neural Network predictions
-  **Alert system** that flags countries crossing critical indicator thresholds

---

## 🛠️ Tools & Technologies

| Category | Tools |
|---|---|
| **Language** | Python 3.10+ |
| **Data Analysis** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn, Plotly |
| **Machine Learning** | Scikit-learn (Logistic Regression, Decision Tree, Random Forest) |
| **Development Environment** | Google Colab, Jupyter Notebook |
| **Reporting** | Power BI, PowerPoint (PPTX), HTML Dashboard |
| **Version Control** | Git, GitHub |

---

## 👤 Author

**[Vinoth Ramar]**  
Data Science Intern · SyntecxHub · April 2026  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/vinoth-ramar)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github)](https://github.com/vinothramar66)

---

## 🏷️ Tags

`data-science` `machine-learning` `economic-crisis` `risk-prediction` `random-forest` `exploratory-data-analysis` `python` `pandas` `scikit-learn` `power-bi` `capstone-project` `internship`

---

<div align="center">

*Submitted as part of SyntecxHub Data Science Internship Program — Task 4, Capstone Project 4*

</div>
