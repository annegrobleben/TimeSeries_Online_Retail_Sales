This notebook is based on an assignment done as part of a Master in Data Science & AI at Nuclio Digital School, it shows how to create a forecasting model that predicts online retail store revenue.

The assignment is split into three main parts: data understanding, data cleaning and model buidling. When building and evaluating the model special attention is paid to the Recall score, the model's ability to detect true positives as such. We begin with four different models: a decision tree, a logistic regression, a random forest and a gradient boosting classifier. The logistic regression and the gradient boosting classifier perform significantly better than the other two models, which is why only those two are optimized further.

0) Import libraries
1) Introduction and Preprocessing: Descriptive Analysis
- 1.1) Check datatypes
- 1.2) Run skimpy analysis
1.3) Univariate analysis
1.4) Add further columns for the analysis: Profit (quantity times unit price), month, day of the week
1.5) Data wrangling
1.5) Stationarity Analysis
1.6) Autocorrelation and partial autocorrelation
1.7) Decomposition of the components of the time series
2) Models Development
2.1) SARIMAX
2.1.1) Model building
2.1.2) Model prediction
2.1.3) Model adjustment
2.2) Auto ARIMA
2.2.1) Model building
2.2.2) Model prediction
2.3) Prophet
2.3.1) Model building
2.3.2) Make predictions
2.4) XGBoost
2.4.1) Model building
2.4.2) Model predictions
2.4.3) Model optimization
2.5) KNN
2.5.1) Model building
2.5.2) Model predictions
3) Results analysis and model selection
3.1) Model comparison
3.2) Model Selection and final forecast
This notebook was created in Google Colab. In order to run it in Google Colab the attached csv-files "heart_disease_data.csv" and "data_dictionary" need to be added to "MyDrive" in Google drive in a folder named "SupervisedMachineLearningn" so that the code cell 4 and 5 can be run properly. In case that this notebook is run in an application that is different from Google Colab part "1.1 Import dataet and data dictionary" needs to be adjusted beforehand.
