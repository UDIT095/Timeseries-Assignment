# Forecasting Exchange Rates using Time Series Analysis

## 📌 Project Title  
**Forecasting Exchange Rates using ARIMA & Exponential Smoothing**

---

## 🎯 Objective  
This project aims to forecast the USD to AUD exchange rate using two powerful time series forecasting methods:  
- **ARIMA (AutoRegressive Integrated Moving Average)**  
- **Exponential Smoothing (ETS)**  

The goal is to analyze, model, and compare the effectiveness of these techniques on real-world exchange rate data.

---

## 📁 Dataset  
The dataset used in this project is `exchange_rate.csv`, which includes historical exchange rates:

| Column        | Description                                 |
|---------------|---------------------------------------------|
| `date`        | Date and time of observation (e.g., 01-01-1990 00:00) |
| `Ex_rate`     | Exchange rate value (USD to AUD)            |

---

## 📄 Files in this Repository  
- `exchange_rate.csv`: The dataset used for forecasting  
- `Timeseries.docx`: Project document detailing objectives, dataset, and tasks  
- `Timeseries.ipynb`: Jupyter notebook containing the full analysis and implementation

---

## 🛠️ Tools and Libraries Used  

- `pandas` — data manipulation  
- `numpy` — numerical computations  
- `matplotlib.pyplot` — visualization  
- `statsmodels.api` — statistical modeling and forecasting  
- `statsmodels.tsa.arima.model.ARIMA` — ARIMA modeling  
- `statsmodels.tsa.holtwinters.ExponentialSmoothing` — ETS modeling  
- `sklearn.metrics` — forecast evaluation (MAE, RMSE, MAPE)  
- `statsmodels.graphics.tsaplots` — ACF/PACF plots  
- `statsmodels.tsa.stattools.adfuller` — stationarity testing (ADF test)

---

## 🔁 Workflow  

### 📊 Part 1: Data Preparation and Exploration  
- Parse `date` and set as index  
- Rename `Ex_rate` to `AUD`  
- Plot the time series  
- Perform stationarity check using the **ADF test**  
- Apply **first-order differencing** if needed  

### 🧠 Part 2: ARIMA Model  
- Use **ACF** and **PACF** plots to select parameters (p, d, q)  
- Fit **ARIMA(1,1,0)** based on results  
- Conduct **residual diagnostics**  
- Forecast future values  

### 📈 Part 3: Exponential Smoothing Model  
- Apply **Simple Exponential Smoothing**  
- Fit model and generate forecasts  
- Compare visually with ARIMA  

### 📐 Part 4: Model Evaluation  
Evaluate both models using:
- **MAE**: Mean Absolute Error  
- **RMSE**: Root Mean Squared Error  
- **MAPE**: Mean Absolute Percentage Error  

| Metric | ARIMA (1,1,0) | Exponential Smoothing |
|--------|---------------|------------------------|
| MAE    | 0.1345        | 0.1601                 |
| RMSE   | 0.2054        | 0.2201                 |
| MAPE   | 0.2279        | 0.2441                 |

🔎 **Insight**: ARIMA shows superior performance across all metrics.

---

## 📝 Conclusion  
- ARIMA outperforms Exponential Smoothing for this dataset.  
- It better captures the underlying structure and trends of exchange rates.  
- Exponential Smoothing remains a valid baseline model, especially when seasonality and trends are weak.

---

## ▶️ How to Run  

1. **Clone the repository**  
```bash
git clone https://github.com/yourusername/exchange-rate-forecasting.git
cd exchange-rate-forecasting
```

2. **Install dependencies**  
```bash
pip install pandas numpy matplotlib statsmodels scikit-learn
```

3. **Launch Jupyter Notebook**  
```bash
jupyter notebook
```

4. **Open and run** `Timeseries.ipynb`

---

## 📬 Contact  
For any queries, feel free to open an issue or reach out!
