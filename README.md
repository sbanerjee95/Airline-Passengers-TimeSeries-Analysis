# Airline-Passengers-TimeSeries-Analysis
Forecasting number of passengers for airlines using ARIMA model in python.

Author: Subhajit Banerjee

![171001-max-inaugural_006-source](https://user-images.githubusercontent.com/17608830/114341611-cdbc1100-9b77-11eb-95c7-2a0a634a124d.jpg)

### Introduction
In this project, I wanted to check if the air passenger data is seasonal, which can help with developing future bussiness strategies for companies serving the tourism industry. Next, with further data analysis I tested several ARIMA and SARIMA models and determined the best fit. Last, I predicted a full cycle of data with the final SARIMA model.

Important Files:
* international-airline-passengers.csv : Airline passengers dataset.
* airline-passengers-analysis.ipynb : Jupyter notebook file containing the time series analysis.

### Data Overview
This dataset contains monthly records of number of air passengers from the year 1949 to 1960.

There are 2 attributes:
1. Month: Contains the month & year.
2. International airline passengers: monthly totals in thousands. Jan 49 ? Dec 60: Contains the total number of passengers travelled in that month.

![Capture](https://user-images.githubusercontent.com/17608830/114342241-24761a80-9b79-11eb-9c4d-4a6e3de29007.PNG)

First, we ploted the time series of the passengers of 144 successive months from 1949 to 1960. There seems to have a seasonal variation every year. Specifically, a clear peak appears around the middle of every year.

### Decomposing Time Series
Usually, time series can be decomposed into three components: trend components and random components, and seasonal components.

A simple, additive decomposition model for a time series can be written as:

#### Y<sub>t</sub>=m<sub>t</sub>+s<sub>t</sub>+e<sub>t</sub>

where m<sub>t</sub> is the trend, s<sub>t</sub> is the seasonality, and e<sub>t</sub> is the random component.

### Methods and Tools
* Python
* ARIMA
* Augmented Dickey-Fuller Test
* ACF and PACF
* Statsmodels
* SARIMA

### Final forecasting using SARIMA model

![Capture](https://user-images.githubusercontent.com/17608830/114343829-59d03780-9b7c-11eb-81a9-1582de6309dd.PNG)

The orange line attached at the end represents the forecasts, with the 95% prediction intervals as grey shaded area. It is clear that the predictive cycle follows the same trend as those observed records.
