ARIMA

Autoregressive Integrated Moving Average (ARIMA): Statistical model for forecasting time series data
Autoregressive (AR): Past values -> Future values
Integrated (I): Differencing used to make data stationary
Moving Average (MA): Incorporate past errors (Predicted - Actual) into future predictions
How to decide AR and MA values? PACF and ACF … To be discussed
Important: Works only on stationary data
Code: arima_gold_prices_timeseries.py
Drawback: Does not consider seasonal fluctuations, so predictions may not be good … Solution: SARIMAX

---

ACF

Auto Correlation Function (ACF) is a regression model that tells us about the correlation of y with its own lags, i.e.
Between y and lag1y
Between y and lag2y
Between y and lag3y
…
Generally, we plot a graph showing lag on the x-axis and the correlation of today’s value with the lag value on the y-axis

---

PACF

Partially Auto Correlation Function (PACF) is similar to ACF
Conveys the relationship of y with its lags, but after removing the effects of the intermediate lags
Example: Here, if we want to see relationship between y and lag3y then it does so after removing the effects of lag1y and lag2y

![image](https://github.com/user-attachments/assets/64adf400-7879-4953-b7e0-e29ca628ccd7)
Conveys the strength of lag3y only

---

Creating a Time Series – SARIMAX

Seasonal Autoregressive Integrated Moving Average Exogenous model (SARIMAX)
Seasonality occurs when certain patterns are not consistent, but appear periodically
So, a simple autoregressive component would not describe that data well
Example: Low sale in November will result into a similar prediction for December (incorrect), but actual high sale in December will result into a similar prediction for January (also incorrect)
Here, SARIMAX comes into picture
