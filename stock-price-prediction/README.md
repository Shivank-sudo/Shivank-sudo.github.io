# Stock Price Prediction (Coming Soon)
This project will use LSTM neural networks to forecast stock prices.

Status: 🟡 In Progress


As a baseline, a naive forecast model was used, assuming each day’s price would equal the previous day’s price. This yielded an RMSE of approximately $3.40. Any advanced model must outperform this baseline to be considered useful.

Linear Regression was used to model closing prices as a function of time. However, with an RMSE of ~31.42, it significantly underperformed compared to the naive forecast baseline (~3.40). This indicates that a simple linear model cannot capture the non-linear and dynamic nature of stock price movements.

Polynomial Regression (degree 3) was used to model the curved trend in stock prices over time. However, it resulted in a higher RMSE (34.57) than even Linear Regression. This suggests that polynomial models tend to overfit the training data and fail to generalize, especially with noisy financial time series like stock prices.

The ARIMA model does not seem to be the best choice here. It is outperformed by simpler models like Naive Forecast and Linear Regression in this case.

This is common for stock prices because they exhibit nonlinear, volatile patterns that ARIMA may not be suited to capture.