# ⛽ Fuel Price Forecasting and Strategic Insights

This repository contains a complete pipeline for forecasting fuel prices in Brazil and generating actionable business insights. It includes data processing, exploratory data analysis (EDA), time series and machine learning modeling, and strategic recommendations.

## 📁 Project Structure

| Notebook | Description |
|----------|-------------|
| `01_data_quality.ipynb` | Data loading, cleaning, transformation, and enrichment (e.g., monthly aggregation, volatility, lags) |
| `02_EDA.ipynb` | Exploratory Data Analysis including seasonality, price trends, and correlation patterns |
| `03_Model_Selection.ipynb` | Forecasting models (ARIMA, SARIMAX, Prophet, LightGBM, HistGradientBoosting, and Hybrid ARIMA + ML) with performance evaluation |
| `04_Model_Tuning.ipynb` | Training and tuning XGBoost and LightGBM models separately by product |
| `05_insights.ipynb` | Business insights based on price elasticity, volatility, label analysis, and clustering of states |

## 🧪 Models Used

- **Time Series Models:** ARIMA, SARIMAX, Prophet
- **Machine Learning Models:** LightGBM, XGBoost, HistGradientBoosting
- **Hybrid Models:** ARIMA + Residual ML Modeling

## 📊 Key Features and Engineering

- Monthly volatility and rolling statistics
- Price spread (avg selling – avg purchase)
- Multiple lags for price and demand
- OneHotEncoding for categorical variables
- Winsorization and IQR filtering for robust outlier handling

## 📈 Evaluation Metrics

- MAE (Mean Absolute Error)  
- RMSE (Root Mean Squared Error)  
- R² (Coefficient of Determination)

## 🧠 Strategic Outputs

- **Elasticity Analysis:** Interpreting customer sensitivity to price by region and product  
- **Price Volatility:** Heatmaps and line plots showing instability across time and location  
- **Label Behavior:** Comparing pricing strategy across different reseller brands  
- **State Clustering:** Grouping UFs by pricing behavior using K-Means  
- **Recommendations:** Region-product-specific pricing guidance based on elasticity

## 📌 Forecast Objective

The core forecasting task is to predict `avg_preco_venda` (average selling price) for each fuel product for:

- June 2024
- July 2024
- August 2024

## ✅ Dependencies

All required libraries are imported in each notebook. You can install them with:

```bash
pip install -r requirements.txt
```

Or install the major ones manually:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn lightgbm xgboost statsmodels pmdarima plotly geopandas
```