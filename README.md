# Automotive-Sales-Forecasting
## Predicting automotive sales in Greece using Google Trends

This repository contains the code of my dissertation in which I try to forecast automotive sales in Greece for passenger vehicles. To do that I use Google Trends data and other variables such as the unemployment rate, the GDP, fuel prices, the Athens Stock Exchange General Index and of course past vehicle sales data.
I do use of several Forecasting Methods such as Exponential Smoothing, ARIMA, Linear Regression, Decision Tree Regression, Random Forest Regression and Support Vector Regression.
More specifically one of the main objectives of this dissertation is to examine if alternative sources of data (in this case Google Trends Times Series related to a car brand) can improve the forecasting accuracy of predictive models. Additionally it is examined if these new models can outperform older "traditional" forecasting methods.
The forecasts are monthly and their time horizon is 12 months ahead.
The brands for which the sales forecasting is performed are four (TOYOTA, AUDI, OPEL, FORD). The predictions concern aggregatively all the passenger vehicle models of each brand.

The following steps are followed:

### 1 Data Importing and Manipulation
* #### 1.1 Import Monthly Sales Data
  In [Data_Sales_collection.ipynb](Notebooks/Sales_data_collection.ipynb) I imported all the monthly sales data for the selected car brands from multiple excel   files downloaded in a folder into one.

* #### 1.2 Import Google Trends and Economic Data
  At the [Data_Import.ipynb](Notebooks/Data_Import.ipynb) notebook I import the rest of the data needed as independent variables for the predictions


### 2 Preliminary Analysis
In this notebook [Preliminary_Anlysis.ipynb](Notebooks/Preliminary_Analysis.ipynb) I calculated mostly correlations between the variables to get insights about their predictive power. I also tried to find the optimal lag perfroming statsmodels cross-correlation 


### 3 Forecasting 
At the [Predictions.ipynb](Notebooks/Predictions.ipynb) notebook I runned the forecasts for 12 months time horizon. For each car brand I built 12 predictive models using various forecasting methods including Exponential Smoothing, Arima, AutoRegression, Decision Tree Regression, Random Forest Regression, Linear Regression and Support Vector Regression. I didn't perform hyperparameter tuning (GridSearch etc.) except only in Auto Arima and Auto Exponential Smoothing which the hyperparameter tuning was integrated at the package. The data were splitted in a train and a test set, the metrics that were used to measure the accuracy of the forecasts were the Root Mean Square Error, the Mean Absolute Error and the Mean Absolute Percentage Error

## Conclusion
After running the forecasts I managed to built some quite robust models (mainly for the TOYOTA brand), but the most important is that it became obvious the positive contribution of Google Trends data to the accuracy of the predictive models. In one case an almost 18% improvement of accuracy was accomplished by inserting Google trends Data in the model.


Below you can see a graph of the predicted (with the best performing model 5) and actual values of the TOYOTA automotive sales.

![TOYOTA_model05](https://user-images.githubusercontent.com/95256482/151883353-6b7bc584-8c74-4837-ae09-ef9de60862a5.png)


You can find the full document of my dissertation in greek at this link [https://dspace.lib.ntua.gr/xmlui/handle/123456789/54664](https://dspace.lib.ntua.gr/xmlui/handle/123456789/54664).
