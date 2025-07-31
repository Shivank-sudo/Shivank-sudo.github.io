# Stock Price Prediction (Coming Soon)
This project will use LSTM neural networks to forecast stock prices.

Status: 🟡 In Progress


As a baseline, a naive forecast model was used, assuming each day’s price would equal the previous day’s price. This yielded an RMSE of approximately $3.40. Any advanced model must outperform this baseline to be considered useful.

Linear Regression was used to model closing prices as a function of time. However, with an RMSE of ~31.42, it significantly underperformed compared to the naive forecast baseline (~3.40). This indicates that a simple linear model cannot capture the non-linear and dynamic nature of stock price movements.

Polynomial Regression (degree 3) was used to model the curved trend in stock prices over time. However, it resulted in a higher RMSE (34.57) than even Linear Regression. This suggests that polynomial models tend to overfit the training data and fail to generalize, especially with noisy financial time series like stock prices.

The ARIMA model does not seem to be the best choice here. It is outperformed by simpler models like Naive Forecast and Linear Regression in this case.

This is common for stock prices because they exhibit nonlinear, volatile patterns that ARIMA may not be suited to capture.

Random Forest with rmse 36.23 performs better than ARIMA but still worse than Naive Forecast and Linear Regression. Random Forest improved over ARIMA by capturing more complex relationships (nonlinear) between stock prices and past values.

Why Random Forest Was Not Much Better: Stock price volatility: Random Forest might struggle to capture extreme market fluctuations, as it doesn't account for external factors like market news, earnings reports, etc.

Lack of time-based features: While Random Forest uses lagged data, it still lacks true sequential memory (like LSTM or ARIMA with seasonal adjustments).

Even for Optimized Random Forest RMSE: 35.73 — A small improvement from the previous 36.23, but still behind the Linear Regression (31.42) and Naive Forecast (3.40).

This suggests that Random Forest, despite its ability to capture non-linear relationships, still struggles to match the performance of simpler models for stock prediction in this case.