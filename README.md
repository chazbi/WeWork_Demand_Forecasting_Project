# WeWork
This is the demand forecasting project I've done at WeWork. The project aims to incorporate market demand into predicting WeWork's building occupancy and empowering pricing strategies. 

The data cleaning & manipulation pseudo-code can be found in the SQL file while the feature engineering and model training pseudo-codes can be found in the R file. The models explored are the linear regression, random forest and XGBoost.

The XGBoost model learns the metrics on market demand, location attributes, and historic performance. Having learnt the patterns from January 2015 to April 2019, the model predicts the building-level occupancy for May, June, July of 2019. The predictions consistently fall within 3% margin of errors around the actual prediction.

--------------------------------------------A list of variable used----------------------------------------------------
The demand proxies used include,
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
 
 The historic performance considered are,
 * last 3 month's location average occupancy
 * last 3 month's churn rate
 * year
 * month
