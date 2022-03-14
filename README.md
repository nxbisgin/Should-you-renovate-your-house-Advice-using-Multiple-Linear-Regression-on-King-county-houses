# Providing Advice As a Real Estate Agent for Kent County Houses

## Overview

This project aims to provide advice to home buyers and sellers in Kent County. For sellers, the aim is to develop a machine learning model that can predict a house's price given its various features, so that the seller will decide on the selling price. On the other hand, the predicted price will help the buyer to understand if the house is marketed at a fair price. Another goal of the project is to provide advice on renovations, if that will help increase the price or not,

The data is provided by Flatiron school and collected from the Kaggle. 


## Data Understanding


This project uses the King County House Sales dataset, which can be found in  `kc_house_data.csv` in the data folder in this GitHub repository. The description of the column names can be found in `column_names.md` in the same folder. 

Kent County House Prices Data includes the following information:

-Price
-Sale Date, Year Built, Renovation Date
-Number of bedrooms, bathrooms, floors
-Waterfront, view
-Condition, grade
-Sqft of living area, lot, basement, above and sqft of living area and lot for 15 nearest neighbors
-Zip Code, latitude, longitude

Price Range
-Min: $78k
-Max: $7.7M
-Avg: $540k


## Business Problem


I develop this project for a real estate agency that makes recommendations to sellers on home renovations and to buyers/sellers on the price of the house. The problems I will focus on are below:

Will the price of the house increase if renovation is done?

Is the seller's price reasonable for the house given the attributes?

## Model

I developed a multiple linear regression model to predict the house prices.

The model can explain ~56% of variability in data.

The model uses the following features to predict the price:
* Grade
* Living area
* Has basement or not
* On waterfront or not
* Renovated or not
* Number of floors

The model formula is approximately like below:
Price ~=   1.28*Grade + 1.15*Living area + 1.07*Has basement + 1.05*On waterfront + 1.04*Renovated + 1.008*Number of floors


## Results


Buyer:
-Given the features of the house, is the price reasonable?
-I can predict the house price with 56% accuracy.

Buyer:
-Which features are most predictive of the price?
-Overall Grade of the house determined by King County: Related to construction and design of the house. Ranges from 1 to 13, from very poor to excellent.
Living Area: Square footage of living space in the house.

Buyer:
-Should I renovate my house?
-Renovating the house will increase the log price of the house by 0.0423, which means the new price will be 1.04 times the old price. If the house is worth $100k, it will become  $104k after renovation. Since the renovation will certainly cost more than $4k, I do not recommend renovations.


## Next Steps

Zip code: Information about zip code is not included in the model. I may need to go deeper into zip codes to incorporate zip codes.

Age of house: I believe age of house should be important for predicting the price but could not be used in the model due to non-linear relation. I may use binning to incorporate age into the model.



