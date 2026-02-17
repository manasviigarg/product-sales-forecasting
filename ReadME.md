# 📊 Scenario-Based Sales Forecasting for Inventory Planning

## 📌 Project Overview
This project demonstrates a **decision-driven sales forecasting framework** designed to support **short-term inventory and capacity planning** for a multi-region retail business.

Rather than focusing solely on forecast accuracy, the analysis prioritizes **decision confidence** by using **scenario-based forecasting** to help leadership prepare for demand uncertainty.

Forecast outputs are treated as **inputs to planning**, not as deterministic predictions.

---

## 📂 Repository Structure

```text
├── data/               # Raw datasets (TRAIN.csv, TEST_FINAL.csv)
├── notebooks/
│   ├── product sales forecasting.ipynb              # Core forecasting model & analysis
│   └── product saled forecasting storytelling.ipynb # Visualization & storytelling
├── requirements.txt    # Python dependencies
```

---

## 🎯 Business Objective
To support **quarter-ahead planning decisions**, including:
- Inventory stocking levels
- Capacity and fulfillment readiness
- Risk exposure under demand volatility

Key leadership questions addressed:
- How much inventory should be stocked under different demand conditions?
- Which demand scenarios pose operational or financial risk?
- How sensitive planning decisions are to demand changes?

---

## 🧠 Key Concept: Why Scenario-Based Forecasting?
Traditional single-point forecasts create **false certainty** in uncertain environments.

This project intentionally models **multiple demand outcomes**:
- **Base Case** – Continuation of historical trend
- **Optimistic Scenario** – Demand exceeds expectations
- **Conservative Scenario** – Demand softens below trend

This allows stakeholders to **stress-test decisions before uncertainty materializes**.

---

## 🗂️ Dataset Description
The dataset contains historical retail sales data with the following key attributes:
- Date
- Sales
- Number of Orders
- Discount Indicator
- Holiday Flag
- Store Type
- Region Code

Two datasets are used:
- `data/TRAIN.csv` — Historical data used for analysis and modeling
- `data/TEST_FINAL.csv` — Holdout data for future extensions

---

## 🔧 Tools & Libraries Used
- **Python**
- **Pandas & NumPy** – Data manipulation and feature engineering
- **Matplotlib & Seaborn** – Exploratory data analysis and visualization
- **SciPy** – Hypothesis testing
- **Scikit-learn** – Linear regression modeling
- **Statsmodels** – Time series decomposition (exploratory)

---

## 🔍 Analysis Workflow

### 1. Data Cleaning & Feature Engineering
- Date parsing and time-based feature creation
- Binary encoding for discount flags
- Missing value handling
- Weekly and monthly temporal features

---

### 2. Decision-Oriented Exploratory Data Analysis
EDA is explicitly tied to **business decisions**, including:
- Time trends and seasonality → rolling planning strategies
- Order volume vs sales → fulfillment capacity alignment
- Discount impact (T-test) → promotion-driven buffer planning
- Holiday effects → proactive inventory positioning
- Store type and regional variability → differentiated stocking policies

---

### 3. Forecasting Approach
A **simple, stable baseline model** (linear trend) is intentionally chosen to:
- Avoid overfitting
- Maintain interpretability
- Support planning rather than precision forecasting

---

### 4. Scenario Construction
Three forward-looking scenarios are created:
- **Base Forecast**
- **Optimistic Forecast (+10%)**
- **Conservative Forecast (–10%)**

These scenarios represent realistic demand bounds rather than extreme assumptions.

---

### 5. Translation from Forecast to Action
Forecast outputs are converted into a **planning summary table**, mapping each scenario to recommended inventory actions.

This step bridges the gap between **analysis and decision-making**.

---

## 📈 Key Outputs
- Scenario-based demand forecasts (next 30 days)
- Planning summary table with actionable recommendations
- Exportable CSV files for BI tools or downstream reporting

Generated files:
- `forecast_scenarios.csv`
- `scenario_summary.csv`

---

## ⚠️ Assumptions & Limitations
- Assumes continuity in historical demand patterns
- Does not account for external shocks (marketing campaigns, macroeconomic changes)
- Intended for **short-term planning**, not long-term financial forecasting

---

## ✅ Appropriate Use
**This analysis is suitable for:**
- Inventory and procurement planning
- Scenario stress-testing
- Operational readiness decisions

**Not suitable for:**
- Long-term revenue commitments
- Pricing strategy without additional modeling
- Financial forecasting without confidence intervals

---

## 🚀 Future Enhancements
- Region-specific forecasting models
- Probabilistic forecasting with confidence intervals
- Promotion and marketing calendar integration
- Advanced time series models (ARIMA / Prophet)

---

## 📌 Final Takeaway
This project demonstrates how forecasting can be reframed from a **prediction exercise** into a **decision-support system**, enabling leadership to act confidently under uncertainty.
