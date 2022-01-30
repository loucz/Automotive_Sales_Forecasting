# Automotive-Sales-Forecasting
## Predicting automotive sales in Greece using Google Trends

This repository contains the code of my dissertation in which I try to forecast automotive sales in Greece for passenger vehicles. To do that I use Google Trends data and other variables such as the unemployment rate, the GDP, fuel prices, the Athens Stock Exchange General Index and of course past vehicle sales data.
I do use of several Forecasting Methods such as Exponential Smoothing, ARIMA, Linear Regression, Decision Tree Regression, Random Forest Regression and Support Vector Regression.
More specifically one of the main objectives of this dissertation is to examine if alternative sources of data (in this case Google Trends Times Series related to a car brand) can improve the forecasting accuracy of predictive models. Additionally it is examined if these new models can outperform older "traditional" forecasting methods.
The forecasts are monthly and their time horizon is 12 months ahead.
The brands for which the sales forecasting is performed are four (TOYOTA, AUDI, OPEL, FORD). The predictions concern aggregatively all the passenger vehicle models of each brand.

The following steps are followed

### 1 Data Importing and Manipulation
#### 1.1 Import Monthly Sales Data


#### 1.2 Import Google Trends and Economic Data
At the notebook below I import the rest of the data needed as independent variables for the predictions
https://github.com/loucz/Automotive-Sales-Forecasting/blob/main/Data_Import.ipynb


### 2 Preliminary Analysis


### 3 Forecasting 
