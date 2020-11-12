# Linear Regression Datasets for Machine Learning
Ref: https://lionbridge.ai/datasets/10-open-datasets-for-linear-regression/


1. [Cancer Linear Regression](https://data.world/nrippner/cancer-linear-regression-model-tutorial)

This dataset includes data taken from cancer.gov about deaths due to cancer in the United States. Along with the dataset, the author includes a full walkthrough on how they sourced and prepared the data, their exploratory analysis, model selection, diagnostics, and interpretation.

2. [CDC Data: Nutrition, Physical Activity, Obesity](https://www.kaggle.com/spittman1248/cdc-data-nutrition-physical-activity-obesity)

From the Behavioral Risk Factor Surveillance System at the CDC, this dataset includes information about physical activity, weight, and average adult diet.

3. [Fish Market Dataset for Regression](https://www.kaggle.com/aungpyaeap/fish-market)

Built for multiple linear regression and multivariate analysis, the Fish Market Dataset contains information about common fish species in market sales. The dataset includes the fish species, weight, length, height, and width.

4. [Medical Insurance Costs](https://www.kaggle.com/mirichoi0218/insurance)

This dataset was inspired by the book Machine Learning with R by Brett Lantz. The data contains medical information and costs billed by health insurance companies. It contains 1338 rows of data and the following columns: age, gender, BMI, children, smoker, region, insurance charges.

5. [New York Stock Exchange Dataset](https://www.kaggle.com/dgawlik/nyse)

Created as a resource for technical analysis, this dataset contains historical data from the New York stock market. The dataset comes in four CSV files: prices, prices-split-adjusted, securities, and fundamentals. Using this data, you can experiment with predictive modeling, rolling linear regression, and more.

6. [OLS Regression Challenge](https://data.world/nrippner/ols-regression-challenge)

The OLS regression challenge tasks you with predicting cancer mortality rates for US counties. The dataset contains data from cancer.gov, clinicaltrials.gov, and the American Community Survey. It is in CSV format and includes the following information about cancer in the US: death rates, reported cases, US county name, income per county, population, demographics, and more.

7. [Real Estate Price Prediction](https://www.kaggle.com/quantbruce/real-estate-price-prediction)

This real estate dataset was built for regression analysis, linear regression, multiple regression, and prediction models. It includes the date of purchase, house age, location, distance to nearest MRT station, and house price of unit area.

8. [Red Wine Quality](https://archive.ics.uci.edu/ml/datasets/wine+quality)

From the UCI Machine Learning Repository, this dataset can be used for regression modeling and classification tasks. The dataset includes info about the chemical properties of different types of wine and how they relate to overall quality.

9. [Vehicle Dataset from CarDekho](https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho)

A useful dataset for price prediction, this vehicle dataset includes information about cars and motorcycles listed on CarDekho.com. The data is in a CSV file which includes the following columns: model, year, selling price, showroom price, kilometers driven, fuel type, seller type, transmission, and number of previous owners.

10. [WHO Statistics on Life Expectancy](https://www.kaggle.com/kumarajarshi/life-expectancy-who)

This dataset contains information compiled by the World Health Organization and the United Nations to track factors that affect life expectancy. The data contains 2938 rows and 22 columns. The columns include: country, year, developing status, adult mortality, life expectancy, infant deaths, alcohol consumption per capita, country’s expenditure on health, immunization coverage, BMI, deaths under 5-years-old, deaths due to HIV/AIDS, GDP, population, body condition, income information, and education.

This is a collection of some thematically related datasets that are suitable for different types of regression analysis. Each set of datasets requires a different technique. A suggested question has that can be answered with regression been posed for each dataset.

## Linear regression (predicting a continuous value):

* [CalCOFI: Over 60 years of oceanographic data](https://www.kaggle.com/sohier/calcofi): Is there a relationship between water salinity & water temperature? Can you predict the water temperature based on salinity?
* [Weather in Szeged 2006-2016](https://www.kaggle.com/budincsevity/szeged-weather): Is there a relationship between humidity and temperature? What about between humidity and apparent temperature? Can you predict the apparent temperature given the humidity?
* [Weather Conditions in World War Two](https://www.kaggle.com/smid80/weatherww2/data): Is there a relationship between the daily minimum and maximum temperature? Can you predict the maximum temperature given the minimum temperature? 

## Poisson regression (predicting a count value):

* [Montreal bike lanes: Use of bike lanes in Montreal city in 2015](https://www.kaggle.com/pablomonleon/montreal-bike-lanes): Is there a relationship between the number of bicyclists who use different bike paths on the same day? Can you predict how many riders there will be on one path given how many are on another?
* [New York City - East River Bicycle Crossings: Daily bicycle counts for major bridges in NYC](https://www.kaggle.com/new-york-city/nyc-east-river-bicycle-crossings): Is there a relationship between the number of bicyclists who cross different bridges in New York?
* (Requires some cleaning) [UK 2016 Road Safety Data: Data from the UK Department for Transport](https://www.kaggle.com/bluehorseshoe/uk-2016-road-safety-data/data) : Is there a relationship between the number of people in the car and the number of casualties in road accidents?

## Logistic regression (predicting a categorical value, often with two categories):

* [The Ultimate Halloween Candy Power Ranking](https://www.kaggle.com/fivethirtyeight/the-ultimate-halloween-candy-power-ranking/): Can you predict if a candy is chocolate or not based on its other features?
* [Epicurious - Recipes with Rating and Nutrition](https://www.kaggle.com/hugodarwood/epirecipes): Can you predict whether a recipe was part of #cakeweek based on whether it its other features?
* (Requires some cleaning) [Competition context and results from 1,559 Kansas City Barbecue Society Barbeque Competitions](https://www.kaggle.com/jaysobel/kcbs-bbq/):: Can you model whether a team will win first place based on their score and the competition they’re at?