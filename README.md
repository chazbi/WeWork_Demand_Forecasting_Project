# Demand-Forecast Project

-- By Charles Haocheng Bi

## Goal
The goal of this project is to forecast demand down to the building level by predicting the metric `occupancy`. The benefits of knowing the occupancy for future months in advance is obvious: it allows the team to decide an optimal discount level to maximize utilization and revenue. 

## Approach
I first identified buildings' key performance drivers: market demand, member experience, historical performance, and the price variable, discount. Then I explored 8 internal data sources and 14 tables to extract 31 location-specific features. I listed a couple proxies for each category below.

  * `Market Demand`: # tour booked per sellable capacity, sales time per desk
  * `Member Experience`: zendesk ticket solve speed, event participation rate
  * `Historical Performance`: avg occupancy of last 3 month
  * `Price Variable`: discount

## Results
The best model is Random Forest with a RMSE = 0.0508. Looking restrospectively, the predictions of the random forest model on average have a mean absolute error less than 3%. This model is recognized by the company leadership as drastically improving discount logic and potentially improving revenue by 9%.

## Applications
This model takes `discount` as an input and output the predicted occupancy according to the discount and other location-specific factors. The application is a one-click discount solution, an internal tool for revenue optimization team.
