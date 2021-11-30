# Car Price predictor: Project Overview
* A web app that estimates the selling price of the used cars to help customers to negotiate from dealers.
* Optimized Random Forest Regressor using RandomizedsearchCV to reach the best model.
* Built a client facing API using flask and deployed into heroku cloud.
* Demo: https://sell-my-car.herokuapp.com/

## Code and Resources Used
**Python Version**: 3.7

**Packages**: pandas, numpy, sklearn, matplotlib, seaborn, flask, pickle

**For Web Framework Requirements**: `pip install -r requirements.txt`

## EDA
![](https://github.com/yashwanth-gurram/car-price-prediction/blob/master/Images/corr.png)

## Model building
* First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.
* I used ExtraTreeRegressor to know the feature importance.

![](https://github.com/yashwanth-gurram/car-price-prediction/blob/master/Images/feature_imp.png)

* I tried Random Forest model and evaluated them using Negative mean squared error and tuned the model using randomized SearchCV to obtain best results.

## Results
The model performed very well.

![](https://github.com/yashwanth-gurram/car-price-prediction/blob/master/Images/pred_scatter.png)

## Productionization
In this step, I built a flask API endpoint that was hosted on a local webserver and deployed into heroku cloud. The API endpoint takes in a request with a list of values from the user and returns estimated selling price.
