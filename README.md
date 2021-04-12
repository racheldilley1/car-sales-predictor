# car-sales-predictor

## Objective:

To build a linear regression model to predict total number of sales in a year for a car based off of certain car specs.

## Aproach:

The features used for baseline modeling were msrp, mpg, car width, car length, car height, wheelbase, speed, horsepower, number of doors, passenger capacity, drive type, fuel tank capacity, fuel type, EPA class, curb weight, and passenger volume. After data acquisition and data cleaning, exploratory data analysis was done using Tableau. Play areound with the interactive dashboard [here](https://public.tableau.com/views/TotalSalesDashboard_16181958948160/Dashboard1?:language=en&:retry=yes&:display_count=y&publish=yes&:origin=viz_share_link).

Feature selection was done to reduce dimensinality, the chance of overfitting, and model complexity. A baseline Lasso Regression model was trained on all features. Features that scored a coeficient of zero (number of doors, tank capacity, car height, and car width), meaning they had no impact on the model, were removed first. 

After intial demsionality reduction, the trainign data was evaluated on a simple linear regression, polynomial regression (second degree and interaction terms only), ridge regression (with and without scaling), and lasso regression (with and without scaling). All models were evaluated to find optimal R-squared value. A lasso with polynomial features scored the highest, however a simple linear regression was chosen due to the small differences in scores and in order to choose a simpler model.

Feature engineering was performed to optimize the r-squared score, adding interaction terms and polynomial terms and also trying box-cox transformations in order to normalize feature data. After feature engineering, more features were removed (fuel type, passenger volume, car speed, passenger capacity, horsepower, and combined miles per galon), continously remooving features and training a simple linear regression model, optimizing for adjusted R-squared value.

## Techniques:

- Exploratory Data Analysis (Tableau)
- Simple Linear Regression
- Polynomial Regression
- Lasso Regression
- Ridge Regression
- Normalization
- Cross Validation
- Feature Selection (Dimensionality Reduction)
- Feature Engineering (interaction terms, polynomial terms, box-cox transformations)

## Data:

Yearly sales data was collected from [Good Car Bad Car](https://www.goodcarbadcar.net/). Model spec data was webscraped from [Car Specs](https://www.carspecs.us/) with additional data gathered from a [git rep](https://www.reddit.com/r/datasets/comments/b6rcwv/i_scraped_32000_cars_including_the_price_and_115/) and the [EPA](vehq.com).

## Results Summary:

A simple linear regression model was chosen. The features that were selected were: MSRP, drivetrain type, transmission type, curb weight, car length, wheelbase length, fuel type, horsepower, and EPA class. Final model testing on testing data scored an R-squared 0.3. An, R-squared value of .3 tells us that around 30% of the variance in the target variable is explained by the model.
