# WeWork Demand-Forecasting Project
I designed and worked on a bottom-up demand forecasting project during the 10-week summer internship with WeWork. The project aims to incorporate market demand, member experience and historical performance into predicting WeWork's building monthly occupancy and empowering pricing decisions. 

The data cleaning & manipulation pseudo-code can be found in the SQL file while the feature engineering and model training pseudo-codes can be found in the R file. The models explored are the time series moving average, linear regressions, random forest and XGBoost. 

The best model is Random Forest with a RMSE = 0.0508. Looking restrospectively, the predictions of the random forest model on average have a mean absolute error less than 3%.
