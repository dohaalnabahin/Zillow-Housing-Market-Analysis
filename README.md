# Zillow Housing Market Analysis and Time Series Forecasting

An end-to-end data science and visualization project focused on processing, analyzing, and forecasting real estate prices across major U.S. states using Zillow home value data (2000–2020).

---

## 📁 Repository Structure
```text
├── Data/
│   └── data-for-tableau.csv         # Cleaned dataset filtered for CA, WA, OR, AZ, NV (2010-2020)
├── Time_Series_Analysis.ipynb        # Google Colab notebook containing data prep and models
└── README.md                         # Project documentation and summary
```

---

## 📊 Phase 1: Data Preprocessing and Exploration
The wide-form Zillow housing dataset was restructured into a tidy long-form time series format with the timestamp set as the dataframe index. 

### Key Technical Operations:
* Resampled and grouped spatial home values to a yearly frequency based on calendar beginnings.
* Isolated the target regional baseline including California (**CA**), Washington (**WA**), Oregon (**OR**), Arizona (**AZ**), and Nevada (**NV**).

### 📈 Historical Price Trends (2010 - 2020)
*Below is the yearly aggregated trajectory showcasing historical home values across the five targeted states:*

![Historical Home Values Trend by State](https://github.com)

---

## 🔮 Phase 2: Advanced Time Series Forecasting (Oregon)
The analytical objective of this section was to isolate the State of Oregon (**OR**) and build robust statistical models to forecast the mean home values for the subsequent 12 months.

### 🛠️ Exploratory Insights & Diagnostics
* **Decomposition:** Time series decomposition verified that the seasonal component was negligible compared to the strong cyclical macroeconomic trend.
* **Stationarity Analysis:** Augmented Dickey-Fuller (ADF) testing confirmed non-stationarity ($p\text{-value} = 0.3874$). Automatic optimization utilities suggested a second-order differencing ($d = 2$) to render the series stationary.
* **Model Configurations Evaluated:** Manual ARIMA(1,2,1), Manual SARIMA(1,2,1)x(1,0,1,12), and an algorithmic grid-search using `pmdarima`'s `auto_arima`.

### 🎯 Final Model Convergence & Forecast Results
The automated search systematically selected the **ARIMA(0, 2, 0)** structure based on information criteria and error optimization. 

* **Final Month Predicted Value:** $337,253.12
* **12-Month Percent Change:** +5.71%

![Oregon True 12-Month Future Forecast](https://github.com)

---

## 🎨 Phase 3: Interactive Visualizations Story
A dynamic visual analytics architecture was developed to map geographical and corporate real estate structures.

### 📌 Interactive Presentation Roadmap (Tableau Story Points)
1. **Top 20 Most Expensive Zip Codes:** Vertical bar chart grouped by location and colored proportionally by County name.
2. **Percentage Change Baseline Comparison:** Temporal line plot tracing relative appreciation since 2010, annotating **Washington (WA)** as the highest appreciating market (~95% increase).
3. **Highlight Table of Premium Locations:** Crosstab highlighting home value concentrations filtered dynamically via interactive sliders for December 2020.
4. **Regional Choropleth Map:** Geographic density mapping under a high-contrast Dark theme, with granular county data integrated directly into tooltips.

![Tableau Visual Presentation Overview](https://github.com)

---

## 🔗 Project Deliverables
* **Source Notebook:** [View Jupyter Notebook](./Time_Series_Analysis.ipynb)
* **Tableau Interactive Presentation:** [View Live Tableau Workbook](https://tableau.com)
