# Time-series-forecasting
"In this project, stock price trends are analyzed and predicted over time using machine learning models like ARIMA and LSTM."



### 📈 Stock Price Forecasting using ARIMA and LSTM

This project demonstrates stock price forecasting using **ARIMA** and **LSTM** models. The stock data is sourced using the `kagglehub` API from the dataset: [jacksoncrow/stock-market-dataset](https://www.kaggle.com/datasets/jacksoncrow/stock-market-dataset).

---

## 📦 Dataset

Dataset is programmatically downloaded using:

```python
import kagglehub
path = kagglehub.dataset_download("jacksoncrow/stock-market-dataset")
```

The dataset includes daily stock price data for multiple companies.

---

## 🔧 Features Used

* Stock symbol used: `AAPL` (Apple) and `MSFT` (Microsoft)
* Features used: Only `Close` price
* Models:

  * **ARIMA**: For statistical time series forecasting
  * **LSTM**: For deep learning-based sequence prediction

---

## 📚 Requirements

Install the required Python libraries:

```bash
pip install kagglehub pandas numpy matplotlib statsmodels scikit-learn keras tensorflow
```

---

## 📁 Project Structure

```bash
.
├── stock_forecasting.ipynb   # Your Jupyter Notebook or Python script
├── README.md                 # Project documentation
└── requirements.txt          # (Optional) Python dependencies
```

---

## 🚀 How to Run

### 1. Download and Load Dataset

```python
import kagglehub
path = kagglehub.dataset_download("jacksoncrow/stock-market-dataset")

import os
import pandas as pd

csv_path = os.path.join(path, "stocks", "AAPL.csv")  # or "MSFT.csv"
df = pd.read_csv(csv_path)
```

---

### 2. ARIMA Forecasting

* Convert Date column to datetime
* Plot the closing price
* Train ARIMA(5,1,0) model
* Forecast next 30 days and plot

---

### 3. LSTM Forecasting

* Normalize `Close` prices using `MinMaxScaler`
* Create time-series dataset using previous 60 days
* Build LSTM model
* Train model and evaluate predictions
* Plot predicted vs actual prices

---

## 📊 Results

* **ARIMA** provides a good short-term forecast based on recent trends.
* **LSTM** learns complex sequential patterns and offers better long-range predictions.
* **ARIMA**: Statistical model best for stationary data
* **LSTM**: Deep learning RNN model suitable for time-series prediction

---

