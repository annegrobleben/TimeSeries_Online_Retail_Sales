This notebook is based on an assignment done as part of a Master in Data Science & AI at Nuclio Digital School, it shows how to create a forecasting model that predicts online retail sales profit.

The assignment is split into three main parts: descriptive analysis, models development and model selection. Five different types of models are built, SARIMAX, Auto ARIMA, Prophet, XGBoost and KNN. The models are evaluated based on the mean absolute error, the root mean squared error and the mean absolute percentage error. After finetuning some hyperparameters the XGBoost model turns out to be the best-performing model considering all three metrics. To make the final forecast a pipeline including a scaler, a deseasonalizer and the hampel filter is set up based on this XGBoost model.

0) Import libraries
1) Introduction and Preprocessing: Descriptive Analysis
- 1.1) Check datatypes
- 1.2) Run skimpy analysis
- 1.3) Univariate analysis
- 1.4) Add further columns for the analysis: Profit (quantity times unit price), month, day of the week
- 1.5) Data wrangling
- 1.5) Stationarity Analysis
- 1.6) Autocorrelation and partial autocorrelation
- 1.7) Decomposition of the components of the time series
2) Models Development
- 2.1) SARIMAX
- 2.2) Auto ARIMA
- 2.3) Prophet
- 2.4) XGBoost
- 2.5) KNN
3) Results analysis and model selection
- 3.1) Model comparison
- 3.2) Model Selection and final forecast
  
This notebook was created in Google Colab. In order to run it in Google Colab the attached csv-file "online_retail_sales.csv" needs to be added to "MyDrive" in Google drive in a folder named "TimeSeries" so that the code cell 4 and 5 can be run properly. In case that this notebook is run in an application that is different from Google Colab part "1) Introduction and Preprocessing: Descriptive Analysis" needs to be adjusted beforehand.
