# 📊 Scenario-Based Sales Forecasting for Inventory Planning

## 📌 Project Overview
This project demonstrates a **decision-driven sales forecasting framework** designed to support **short-term inventory and capacity planning** for a multi-region retail business.

Rather than focusing solely on forecast accuracy, the analysis prioritizes **decision confidence** by using **scenario-based forecasting** to help leadership prepare for demand uncertainty.

Forecast outputs are treated as **inputs to planning**, not as deterministic predictions.

---

## 📂 Repository Structure

```text
├── product-sales-forecasting.ipynb              # Core forecasting model & analysis
├── product-sales-forecasting-storytelling.ipynb # Visualization & storytelling
├── TRAIN.csv                                    # Historical training data
├── TEST_FINAL.csv                               # Holdout data for future extensions
├── requirements.txt                             # Python dependencies
└── ReadME.md                                    # This ReadME file
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
Traditional single-point forecasts create **false certainty** in uncertain environments. This project intentionally models **multiple demand outcomes** to allow stakeholders to **stress-test decisions before uncertainty materializes**.

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
- `TRAIN.csv` — Historical data used for analysis and modeling
- `TEST_FINAL.csv` — Holdout data for future extensions

---

## 🔧 Tools & Libraries Used
- **Python**
- **Pandas & NumPy** – Data manipulation and feature engineering
- **Matplotlib & Seaborn** – Exploratory data analysis and visualization
- **SciPy** – Hypothesis testing
- **Scikit-learn** – Linear regression modeling
- **Statsmodels** – Time series decomposition (exploratory)

A full list of dependencies is available in `requirements.txt`.

---

## 🚀 How to Run
1.  Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
2.  Run the `product-sales-forecasting.ipynb` notebook to perform the analysis and generate the forecast outputs.
3.  Run the `product-sales-forecasting-storytelling.ipynb` notebook to see the visualizations and narrative.

---

## 📈 Key Outputs
The `product-sales-forecasting.ipynb` notebook generates the following files:
- `forecast_scenarios.csv`: Contains the base, optimistic, and conservative forecast scenarios.
- `scenario_summary.csv`: A summary table of the expected average sales for each scenario.

---

## ⚠️ Assumptions & Limitations
- Assumes continuity in historical demand patterns
- Does not account for external shocks (marketing campaigns, macroeconomic changes)
- Intended for **short-term planning**, not long-term financial forecasting
