# Bitcoin_prediction
# 📈 Bitcoin Market Capitalization Prediction

## 🔍 Project Overview

This project focuses on predicting **Bitcoin Market Capitalization** using historical market data and machine learning regression models. By leveraging price-related features (Open, High, Low, Close), trading Volume, and temporal attributes (Year, Month, Day), the model learns the underlying relationship that drives market capitalization.

The final model achieves **high predictive performance (≈96–97% R²)**, indicating strong generalization on unseen data.

---

## 🎯 Objective

* Predict **Bitcoin Market Cap** accurately using historical price and volume data
* Apply proper **regression techniques** and evaluation metrics
* Build an **industry-ready ML pipeline** with clean preprocessing and validation

---

## 📊 Dataset Description

The dataset contains daily Bitcoin market data with the following features:

| Feature                 | Description                 |
| ----------------------- | --------------------------- |
| Open                    | Opening price of Bitcoin    |
| High                    | Highest price of the day    |
| Low                     | Lowest price of the day     |
| Close                   | Closing price of Bitcoin    |
| Volume                  | Daily trading volume        |
| Year                    | Year of record              |
| Month                   | Month of record             |
| Day                     | Day of record               |
| **Market Cap (Target)** | Total market capitalization |

> **Note:** Numeric columns such as `Volume` and `Market Cap` were cleaned by removing commas and converting to numeric format.

---

## 🧠 Problem Type

* **Machine Learning Task:** Regression
* **Target Variable:** Market Cap (continuous)
* **Why Regression?** Market capitalization is a continuous numeric value, not a class label.

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing

* Removed formatting issues (commas in numeric columns)
* Feature-target separation
* Train-test split (80–20)
* Feature scaling using **MinMaxScaler**

### 2️⃣ Model Selection

The following models were evaluated:

* Linear Regression (baseline)
* Random Forest Regressor
* **XGBoost Regressor (final model)**

XGBoost was selected due to its ability to capture non-linear relationships and strong performance on structured data.

---

## 🚀 Model Training (XGBoost Regressor)

Key hyperparameters:

* `n_estimators = 300`
* `learning_rate = 0.05`
* `max_depth = 6`
* `subsample = 0.8`
* `colsample_bytree = 0.8`

---

## 📈 Evaluation Metrics

The model was evaluated using standard regression metrics:

| Metric               | Result |
| -------------------- | ------ |
| **R² Score (Train)** | ~0.96  |
| **R² Score (Test)**  | ~0.95  |
| MAE                  | Low    |
| RMSE                 | Low    |

These results indicate **strong predictive accuracy** with minimal overfitting.

---

## 📉 Visualization

* **Actual vs Predicted Scatter Plot**
* **y = x reference line** to visualize prediction accuracy
* Feature importance analysis for explainability

---

## ⚠️ Important Insight

Bitcoin Market Cap is **highly correlated with price-based features**. Since market cap is derived from price × circulating supply, high predictive performance is expected when price information is included.

This relationship is acknowledged and validated through feature importance analysis.

---

## 🧪 Future Improvements

* Time-series forecasting (next-day market cap prediction)
* Lag features and rolling statistics
* Removing potential data leakage features
* LSTM / ARIMA-based forecasting models

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib

---

## 📌 Conclusion

This project demonstrates an end-to-end regression pipeline for predicting Bitcoin market capitalization with high accuracy. It follows best practices in preprocessing, modeling, and evaluation, making it suitable for academic projects, portfolios, and real-world ML applications.

---

## 👤 Author

**Elliot**
Student | Machine Learning Enthusiast

---

⭐ If you find this project useful, consider giving it a star!
