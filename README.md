# WeWork
This repo covers the core part of my intern project at WeWork (Jun. - Aug. 2019). The project aims to incorporate market demand into predicting WeWork's building occupancy and empowering pricing strategies. 

The demand proxies explored are both location-level demand and city-level demand. They are,
    * pct of rush bookings (i.e. reservations booked within 10 days prior to their move-in date)
    * monthly tour completed/booked
    * tour conversion rate
    * GDP per capital
    * GDP per capital annual growth
    * unemployment rate

Together with metrics on location attribute (maturity, location, etc) and historic performance, the model has an accuracy of 97% meaning that if the actual building occupancy next month is 90%, then the prediction will be consistently fall within (87%, 93%).

The data cleaning & manipulation was done mostly in SQL while the feature engineering and model training were done in R. The models used are the linear regression, random forest and XGBoost.
