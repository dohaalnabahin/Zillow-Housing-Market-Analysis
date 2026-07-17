# Zillow Housing Market Analysis & Forecasting

An end-to-end data science and visualization project analyzing U.S. housing prices (2000–2020).

---

## 📁 Repository Structure
* `Data/data-for-tableau.csv` : Cleaned dataset (CA, WA, OR, AZ, NV).
* `Time_Series_Analysis.ipynb` : Google Colab notebook (Data prep & models).

---

## 📊 Phase 1 & 2: Time Series Analysis & Forecasting (Oregon)

### 📈 Historical Price Trends
![Historical Home Values](https://github.com)

### 📉 Modeling & Diagnostics Summary

| Model Configuration | AIC Score | Key Diagnostic Finding |
| :--- | :--- | :--- |
| **Manual ARIMA(1, 2, 1)** | 3457.674 | Non-significant coefficients; residual autocorrelation remains. |
| **Manual SARIMA(1,2,1)x(1,0,1,12)** | 3393.397 | Significant seasonal components; lower error than manual ARIMA. |
| **Auto-ARIMA (ARIMA(0, 2, 0))** | 3453.299 | **Selected Model:** Captures optimal stochastic trend after differencing. |

### 🔮 12-Month Future Forecast Results
![Oregon Future Forecast](https://github.com)

* **Predicted Final Month Value (Dec 2019):** $337,253.12
* **12-Month Expected Percent Change:** +5.71%

---

## 🎨 Phase 3: Interactive Visualizations (Tableau Story)

| Story Point | Visualization Type | Key Analytical Insight |
| :--- | :--- | :--- |
| **Point 1** | Top 20 Zip Codes Bar Chart | Displays highest-value properties grouped by County Name. |
| **Point 2** | Percentage Change Line Plot | **Washington (WA)** achieved the highest growth (~95% increase). |
| **Point 3** | Premium Locations Highlight Table | Dynamic crosstab showcasing property concentrations (Dec 2020). |
| **Point 4** | Regional Choropleth Map | Dark-themed geographic density mapping with detailed tooltips. |

![Tableau Presentation Overview](https://github.com)

---

## 🔗 Project Deliverables
* **Jupyter Notebook:** [View Notebook Source](./Time_Series_Analysis.ipynb)
* **Interactive Presentation:** [View Live Tableau Workbook](https://tableau.com)
