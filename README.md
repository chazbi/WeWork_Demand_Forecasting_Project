# Demand-Forecast Project

-- By Charles (Haocheng) Bi

## Goal
The project goal is to forecast demand down to the building level by predicting the metric `occupancy`. The benefits of knowing the occupancy for future months in advance is obvious: it allows the team to decide an optimal discount level to maximize utilization and revenue. 

## Approach
I first identified buildings' key performance drivers: market demand, member experience, historical performance, and discount - the price variable. I explored 8 internal data sources and 14 tables to extract 31 location-specific features. I listed a couple proxies for each category below.

  * `Market Demand`: # tours booked/completed per sellable capacity, sales time per desk (in days)
  * `Member Experience`: zendesk ticket solve speed (in days), event participation rate
  * `Historical Performance`: avg occupancy of last 3 month
  * `Price/Decision Variable`: discount

## Results
The best model is Random Forest with a RMSE = 0.0408. Looking restrospectively, the predictions of the random forest model on average have a mean absolute error less than 3%. This model is recognized by the company leadership as drastically improving discount logic and potentially improving monthly revenue by 9.3% by minimizing unused space.

## Business Impacts
The business impacts of the model were three-hold. The first and most important one, it reinforced pricing logic and optimized revenue. As the model output an occupancy rate at any pricing level, it could be used as a simple one-click discount solution producing the optimal discount level. Second, it pivoted the WeWork sales strategy from new user acquisition to client retention. Lastly, it highlighted the importance of an event-driven WeWork community to increase member satisfaction. The project was presented to 5 teams within WeWork and recognized highly by the company management. In August 2019 alone, with the help of the model, 82 overpriced buildings and 64 underpriced buildings could be repriced for a **$2.4 million revenue gain**.

## Applications - Maximize Revenue
The model takes in `discount` as an input and output the predicted occupancy according to the discount and other location-specific factors. One major application is a one-click discount solution, which outputs a projected occupancy rate according to the discount level. Say 80% occupancy is projected at 10% discount while 85% occupancy at 15% discount. Thus, the team can maximize revenue based on the `price (1-discount%)` and `projected occupancy`.

#### Disclaimer
TThe purpose of this repository is strictly for coding skill demonstrations. All rights reserved.
