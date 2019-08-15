# WeWork
This repo covers the core part of my intern project at WeWork (Jun. - Aug. 2019). The project aims to incorporate market demand into predicting WeWork's building occupancy and empowering pricing strategies. 

The demand proxies explored include,
*   location-level demand
       * pct of rush bookings (i.e. reservations booked within 10 days prior to their move-in date)
       * monthly tour completed/booked
       * tour conversion rate
*   city-level demand
       * GDP per capital
       * GDP per capital annual growth
       * unemployment rate
 
 The location attributes considered are,
 *   geographical factors
       * city
       * market
       * region
 *   sales factors
       * month_opened
       * pct of presale reservables
 *   community factors
       * Zendesk satisfaction
       * Zendesk response time
       * happy hour counts
       * speaker event counts
      
Together with historical performance data, those metrics collectively predict building monthly occupancy rate with an accuracy of **97%**. If the actual building occupancy next month is 90%, the prediction will be consistently fall within (87%, 93%).

The data cleaning & manipulation was done mostly in SQL while the feature engineering and model training were done in R. The models used are the linear regression, random forest and XGBoost.
