# Finance Stock Price Prediction Project

This project provides a robust, repeatable machine learning
for technical analysis and stock price prediction across multiple
independent assets. 

The project consists of two primary stages: 

* Stock Data Analysis: Generating plots for prices of 'Volume', 'High', 'Low', 
  'Close', Market Capital, various Exponential Moving Averages (EMA) and Simple
  Moving Averages (SMA) to define short-term, medium-term, and long-term trends. 
  It also includes stock increase analysis using volatility. 

* LSTM Time Series Modeling: Training an LSTM (Long Short-Term Memory) neural
  network on each stock's historical price data and evaluating its predictive
  accuracy on a held-out test set. 

## Dataset  

Yahoo Finance API was used to fetch historical price data for 5 stocks (Tesla, 
Nvidia, Amazon, Apple, Netflix).  

Stock Date Range: 2020-01-01 to 2025-09-30  

## LSTM Prediction Pipeline 

### Data Preparation
* Scaling: MinMaxScaler   
* Sequence Creation: look_back = 60 
* Train_Test: 80% for training, 20% for testing 

### Model Architecture  
* Layers: LSTM layers with 100 units, epoch with 50 
* Loss function: Mean Squared Error (MSE)
* Optimizer: Adam  

### Performance Metrics  
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)

### Results  

 Metrics for TSLA (Tesla):
 * Mean Squared Error (MSE): 196.0285
 * Root Mean Squared Error (RMSE): 14.0010

 Metrics for NVDA (Nvidia):
 * Mean Squared Error (MSE): 44.3366
 * Root Mean Squared Error (RMSE): 6.6586

 Metrics for AMZN (Amazon):
 * Mean Squared Error (MSE): 28.4483
 * Root Mean Squared Error (RMSE): 5.3337

 Metrics for AAPL (Apple):
 * Mean Squared Error (MSE): 26.9558
 * Root Mean Squared Error (RMSE): 5.1919

 Metrics for NFLX (Netflix):
 * Mean Squared Error (MSE): 839.3671
 * Root Mean Squared Error (RMSE): 28.9718

Since RMSE is the preferred metric, we focus on RMSE values. In case of Tesla, 
RMSE is 14.0010 dollar, indicating that the average dollar error between actual stock
price and predicted stock price is 14.0010 dollar. Thus:  

Error gap between actual stock price and predicted stock prices:  
* Tesla: 14.00 dollar
* Nvidia: 6.66 dollar
* Amazon: 5.33 dollar
* Apple: 5.19 dollar
* Netflix: 28.97 dollar  
