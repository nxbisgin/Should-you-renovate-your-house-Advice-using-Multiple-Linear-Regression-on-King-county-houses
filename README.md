# Should you renovate your house or not?

## Overview

This project aims to provide advice to home buyers and sellers in Kent County. For sellers, the aim is to develop a machine learning model that can predict a house's price given its various features, so that the seller will decide on the selling price. On the other hand, the predicted price will help the buyer to understand if the house is marketed at a fair price. Another goal of the project is to provide advice on renovations, if that will help increase the price or not,

The data is provided by Flatiron school and collected from the Kaggle. 


## Business Problem

In this project, I am acting as a real estate agency that makes recommendations to sellers on home renovations and the price of the house. The problems I will focus on are below:

Will the price of the house increase if renovation is done?

If so, which features should the seller focus on renovation?


## Data Understanding

This project uses the King County House Sales dataset, which can be found in  `kc_house_data.csv` in the data folder in this GitHub repository. The description of the column names can be found in `column_names.md` in the same folder. 

Kent County House Prices Data includes the following information:

- Price
  -Min: $78k
  -Max: $7.7M
  -Avg: $540k
  
![prices](https://raw.githubusercontent.com/nxbisgin/phase-2-project-Kent-County-House-Price-Prediction-Linear-Regression/main/prices.png)
  

- Sale Date, Year Built, Renovation Date
- Number of bedrooms, bathrooms, floors
- Waterfront, view
- Condition, grade
- Sqft of living area, lot, basement, above and sqft of living area and lot for 15 nearest neighbors
-Zip Code, latitude, longitude


## Model

I developed a multiple linear regression model to predict the house prices.

![modelerror](https://raw.githubusercontent.com/nxbisgin/phase-2-project-Kent-County-House-Price-Prediction-Linear-Regression/main/modelerror.png)

The model can explain ~56% of variability in data.


## Most Important Feature: Grade

Price increases most with the increase in the grade of the house.

![grade](https://raw.githubusercontent.com/nxbisgin/phase-2-project-Kent-County-House-Price-Prediction-Linear-Regression/main/grade.png)

If the grade increases by 1 unit, the price increases by 28%.


## Second Most Important Feature: Living Area

Second most effective feature on the price is the living area of the house.

![living_area](https://raw.githubusercontent.com/nxbisgin/phase-2-project-Kent-County-House-Price-Prediction-Linear-Regression/main/living_area.png)

If the living area of the house increases by 10%, the price will increase by 1%.


## Recommendations

- Which features are most effective of the price?
- Overall Grade of the house determined by King County: Related to construction and design of the house. Ranges from 1 to 13, from very poor to excellent.
- Living Area: Square footage of living space in the house.

- Should the house be renovated?
- I would highly recommend renovating the house if the grade of the house is increased or more living area is added by renovation.
