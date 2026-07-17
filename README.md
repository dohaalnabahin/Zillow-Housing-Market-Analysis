# Comprehensive Zillow Housing Market Analysis & Predictive Forecasting

A comprehensive data science project focused on time series exploration, forecasting, and interactive spatial analysis of U.S. housing market trends using Zillow home value data.


---

## 📁 Repository Architecture & Layout
```text
├── Data/
│   └── data-for-tableau.csv         # Restructured regional subset (CA, WA, OR, AZ, NV) for 2010–2020
├── Time_Series_Analysis.ipynb        # Comprehensive Google Colab Jupyter Notebook (Models & Evaluation)
└── README.md                         # Detailed project document dashboard
```

---

## 📊 Phase 1: Data Reshaping & Historical Exploratory Analysis

The initial wide-form raw data columns representing monthly increments were programmatically melted into a long-form time-series format. Home values were aggregated to a clean yearly frequency using statistical mean grouping.

### Regional Tracking Parameters
* **Target Geographic Baseline:** California (CA), Washington (WA), Oregon (OR), Arizona (AZ), Nevada (NV).
* **Target Time Horizon:** Jan 01, 2010, through Dec 31, 2020.

### 📈 Historical Visual Trajectory
*Below is the yearly aggregated trajectory showcasing historical home values across the five targeted states:*

![Historical Home Values Trend by State](https://github.com)

---

## 🔮 Phase 2: Statistical Modeling & Time Series Forecasting (Oregon)

This section isolates the monthly mean home prices for the State of Oregon (OR) from January 31, 2000, through December 31, 2018, to forecast real estate evaluations 12 months into the future.

### 🛠️ Exploratory Stationarity & Structural Analysis
1. **Time Series Decomposition:** Additive decomposition isolated a negligible seasonal component (+200 to -$600) relative to a dominant non-linear economic macro trend ($300k+).
2. **Stationarity Validation:** Augmented Dickey-Fuller (ADF) testing confirmed non-stationarity ($p\text{-value} = 0.3874$). Algorithmic evaluation recommended second-order differencing ($d = 2$).

### 🔬 Model Evaluation & Convergence Dashboard

| Model Configuration Type | Target Hyperparameters | AIC Metric | Key Diagnostic Performance Output |
| :--- | :--- | :--- | :--- |
| **Manual Exploratory ARIMA** | $\text{ARIMA}(1, 2, 1)$ | 3457.674 | AR and MA coefficients failed significance test ($p\text{-value} > 0.05$); residual autocorrelation remained. |
| **Manual Seasonal ARIMA** | $\text{SARIMA}(1,2,1) \times (1,0,1)_{12}$ | 3393.397 | Significant seasonal components; superior AIC scores relative to manual non-seasonal configurations. |
| **Algorithmic Auto-ARIMA** | $\text{ARIMA}(0, 2, 0)$ | 3453.299 | **Selected Final Model:** Optimally isolated the underlying stochastic trend with efficient parameter purity. |

### 🔮 12-Month Predictive Horizon Output (2019)
![Oregon 12-Month Future Forecast](https://github.com)

* **Predicted Final Month Evaluation:** $337,253.12
* **12-Month Projected Growth Rate:** +5.71%

---

## 🎨 Phase 3: Spatial Analytics & Interactive Storytelling Architecture

All visualizations are deployed in a unified interactive Tableau Story. The interface is optimized using high-contrast dark mappings and dynamic dashboard components.

### 📌 Interactive Presentation Blueprint (Tableau Story Points)

| Story Point Sequence | Target Chart Configuration | Visual Attributes & Mappings | Primary Analytical Insight Delivered |
| :--- | :--- | :--- | :--- |
| **Story Point 1** | Localized Premium Ranking | Vertical Bar Graph; Colored by County Name; Top 20 Filter. | Identifies premium housing cost concentrations across core U.S. West Coast metropolitan areas. |
| **Story Point 2** | Percentage Difference Matrix | Multi-Line Chart; Relative to Jan 2010 Baseline; Custom Annotation. | Confirms **Washington (WA)** as the fastest-growing market with a ~95% price expansion over the decade. |
| **Story Point 3** | High-Density Highlight Grid | Colored Square Highlight Matrix; Custom Text Values; Filtered for Top 20. | Displays granular structural home values via interactive Month/Year Single Value Sliders. |
| **Story Point 4** | Spatial Choropleth Map | Dark-Themed Map Background; Full Color Range Gradient; Tooltip Overlay. | Provides detailed geo-density insights down to the Zip Code level with City and County details visible on hover. |

![Tableau Visual Presentation Overview](https://github.com)

---

## 🔗 Live Project Deliverables
* **Jupyter Source Code:** [View Production Notebook Notebook](./Time_Series_Analysis.ipynb)
* **Interactive Tableau Presentation:** [Launch Live Tableau Story Application](https://tableau.com)
