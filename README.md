DATA-SCIENCE_PROJECT---3

Electricity Demand Estimation for Leading Electricity Distributor.

Business Objective : One of leading electricity Distribution Company would like to understand demand for electricity for the next 1-2 years to manage the production of electricity and managing the vendors for the same. It is one of the important exercises to getting accurate estimation of demand so that they can procure or produce the electricity as per the demand.

Solution Data pipelines.
1) Import packages which are crucial, then read respective data file.

2) Data Preprocessing - 
   a. Create Year_Month column and set it as index. Also create Year, Month as separate columns for future reference.
   b. Visualize the data in graphical format for better understanding of the data.
   c. Create pivot table with index = Year and Columns = Month, Values = Electricity_Consumption
   d. Visualize the pivot table data into axes subplot for clear separation.
   
3) Decomposition of data - 
   a. To decompose the data we utilize seasonal decompose package.
   b. Seasonal decompose package contains two types - additive and multiplicative.
   c. Additive decomposition is applied to understand the time series data thoroughly.
   d. Additive decompose is apopiled on to the dataset because when the data is related to time series then level, trend, seasonality and noise are computed. 
   
4) Perform AutoCorrelation and Partial Autocorrelation test to indicate a model would be appropriate for the time series because the ACF cuts after one lag while the PACF shows slowly decreasing trend. 

5) Perform statistical significance test to check whether time series data is stationary or not. Augmented Dickey - Fuller test is used to determine the solution.

6) Apply Exponential Smoothing to focus on trend and seasonal components. This data then used to presentation or to make forecast. 

7) Apply train test split to overcome the problem of overfitting.

8) Perform seasonal ARIMA test for explicitly support to univariate time series data with the seasonal components.

9) Now model can be used to make a forecast. Found the model train error is too minimal hence the model provides higher accuracy.

10) To check accuracy we employ different metrics such as MAPE, RMSE, RMSPE.

11) To forecast the demand of electricity and to visualize the result of the same new line graph is generated along with diagnostics().


