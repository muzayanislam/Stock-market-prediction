
# **Stock Price Prediction and Dynamic Investment Strategy**  

This project uses LSTM models to forecast stock prices for leading tech companies (AAPL, MSFT, GOOG), evaluate prediction performance, and simulate a 5-day dynamic investment strategy based on predicted growth. It integrates time-series forecasting, data scaling, and decision-based portfolio reallocation.


## Objectives

**Stock Price Forecasting**: Predict future stock prices using deep learning.  
- **Model Performance Evaluation**: Use RMSE and visual comparisons to assess model accuracy.  
- **Daily Prediction Analysis**: Predict today's and yesterday’s stock closing prices based on historical trends.  
- **Investment Simulation**: Test a dynamic investment strategy that reallocates capital based on predicted returns.
## Dataset

Historical adjusted closing prices for:

- **Apple (AAPL)**
- **Google (GOOG)**
- **Microsoft (MSFT)**

Each dataset includes:

- Daily adjusted close prices
- Used 100-day sliding windows to train and forecast using LSTM
## Analysis Process

### 1. Model Training & Prediction
- LSTM models trained on each stock’s historical data  
- Applied `MinMaxScaler` for normalization  
- Inverse transformations used to get real-world price predictions  

### 2. Visualization
- Plotted actual vs predicted prices  
- Clear temporal patterns and prediction accuracy were visible  

### 3. Daily Prediction
- Predicted today's closing price using the last 100 days  
- Also predicted using data until yesterday to compare outcomes  

### 4. Investment Strategy Simulation
- Started with £1000, invested initially in AAPL  
- Reallocated to stock with the best predicted growth over 5 days  
- Final investment value remained stable due to low volatility  
## Key findings

LSTM models produced low RMSE, indicating good short-term forecast capability  
- Predictions were slightly overestimated, especially for AAPL  
- Dynamic investment simulation showed no gain or loss, highlighting a need for longer investment windows or more volatile assets
## Recommendations

### Model Enhancement
- Use advanced models (e.g., Bi-LSTM, Transformer-based)  
- Add macroeconomic data and news sentiment analysis  

### Investment Strategy
- Simulate across a longer horizon  
- Include transaction costs and risk management  

### Automation
- Schedule daily predictions  
- Visualize metrics in a live dashboard using Streamlit or Plotly  
## Automation & Reporting

- All workflows automated via Python  

**Logs include:**
- Predicted vs actual prices  
- RMSE outputs  
- Daily portfolio value  