# car-sales-predictor

## Objective:

To build a linear regression model to predict total car sales in a year for a car based off of certain car specs.

## Aproach:

The features used in this model were the mpg, car width, car length, wheelbase, speed, horsepower, number of doors, passenger capacity, drive type, fuel tank capacity, car height, engine type, and price. Feature engineering was performed to eliminate collinear features and to split the data into smaller and larger cars. The trainign data was evaluated on linear regression, polynomial regression (second degree and interaction terms only), ridge regression (with and without scaling), and lasso regression (with and without scaling). All models were evaluated to find optimal R2 and MAE values. 

## Data:

Yearly sales data was collected from goodcarbadcar.net and model spec data was webscraped from carspecs.us

## Results Summary:

A simple linear regression model was chosen. The features that were selected were: the number of doors, passenger capacity, drive type, fuel tank capacity, car length times width, car height, engine type, and price. Final Model testing on testing data showed significant decresse in r2 test score compared to validation score. This indicates that the model is not a good fit and all car specs examined are not good predictors of the total number of cars sold in a year. More data needs to be collected and more car specs need to be considered. 
