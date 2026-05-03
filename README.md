# Time-Series-Modeling-AR-MA-ARMA-ARIMA-SARIMA-
This project demonstrates a complete time series analysis workflow using Python, covering model identification, estimation, diagnostics, and forecasting. The analysis is performed on occupancy data and compares multiple models including AR, MA, ARMA, ARIMA, and SARIMA to identify the best forecasting approach.

## Project Description
This project performs time series analysis and forecasting on occupancy data using statistical models such as AR, MA, ARMA, ARIMA, and SARIMA. The objective is to identify the best model based on diagnostics and forecasting performance.


## Dataset
- File used: `occupancy.xlsx`
- Target variable: `occupancy`

##  Steps Performed

1. **Import Libraries**
   - numpy, pandas, matplotlib, seaborn, statsmodels

2. **Load Data**
   - Read dataset using pandas

3. **Check for White Noise**
   - Applied Ljung-Box test  
   - Result: Data is not white noise (has autocorrelation)

4. **ACF & PACF Analysis**
   - ACF used to identify MA components  
   - PACF used to identify AR components  


## Models Built

### AR Model
- AR(1), AR(2)
- AR(2) performed better based on residual tests  

### MA Model
- MA(1), MA(2)
- Poor performance (residuals not white noise)  

### ARMA Model
- ARMA(1,1), ARMA(2,2)
- Moderate performance  

### ARIMA Model
- ARIMA(2,1,2)
- Best non-seasonal model  
- Lowest BIC and improved residuals
  
### SARIMA Model
- SARIMA(1,1,1)(1,1,1,4)
- Captures seasonality  
- Best overall performance  


## Model Comparison

| Model   | Performance |
|--------|------------|
| AR     | Good |
| MA     | Poor |
| ARMA   | Moderate |
| ARIMA  | Best (non-seasonal) |
| SARIMA | Best overall |

## Key Insights
- Data contains autocorrelation → requires modeling  
- AR models performed better than MA  
- ARIMA improved accuracy significantly  
- SARIMA gave best results due to seasonality  

## How to Run

1. Place dataset (`occupancy.xlsx`) in the working directory  
2. Open the notebook: `time_series_forecasting_occupancy.ipynb`  
3. Run all cells step-by-step  
4. Check model outputs and forecasts  

## Libraries Used
- pandas  
- numpy  
- matplotlib  
- seaborn  
- statsmodels  

## Conclusion
SARIMA is the most effective model for this dataset as it captures both trend and seasonal patterns, leading to better forecasting accuracy.
