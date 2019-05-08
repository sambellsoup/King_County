


# Predicting House Sales Price in King County


## Project Overview

With this data I had a few goals in mind. My short-term goal was to create a model in order to predict the price a house would sell for given a few variables. The dataset taken from Kaggle describes the price at which homes were sold in 2014-2015 as well as several features of the home: like whether it was on the waterfront, square footage, and location. 

<b> Key Questions: </b>
- Can we create a model to predict the price a house would sell for with a relative certainty?
- Which features of the home are most indicative of its value?

## Key Variables
### Target Variable: Price
### Feature Variables:
- id - Simple indexing of each entry in dataset
- date - The date the house was sold
- price - The monetary value the home was sold for in American dollars
- bedrooms - The number of bedrooms in the home
- bathrooms - The number of bathrooms in the home. A half bathroom means a toilet and a sink (no shower), and a quarter bathroom means only a sink.
- sqft_living - The amount of living space in the home.
- sqft_lot - The amount of land the home sits on.
- floors - How many levels the home has. 
- waterfront - Whether or not the home is directly near the water
- view - How good the view has been evaluated to be. This has been measured from 1-4. 1 indicates poor scenery, while 4 indicates very beautiful scenery.
- condition - The level of condition of the home. On a scale of 1-5, what condition is the home currently in? Does it need repairs? A 1 indicates poor condition, while a 5 indicates perfect condition. 
- grade - Measures the quality of materials used to construct the home. On a scale of 1-13. 1 indicates poor quality of materials while 13 indicates the best quality of materials. 
- sqft_above - Measures the amount of space in the home excluding the basement
- yr_built - Reflects the year the home was built
- yr_renovated - Tells the year the home was renovated
- zipcode - The zipcode where the home is.
- lat - Latitudinal coordinate of the home.
- long - Longitudinal coordinate of the home.
- sqft_living15 - Measures the sqft_living of the nearest 15 neighbors.
- sqft_lot15 - Measures the sqft_lot of the nearest 15 neighbors. 

More information can be found on the Kaggle Website <a
href=https://www.kaggle.com/harlfoxem/housesalesprediction>website</a>

## Data Collection and Analysis

Data from this database was examined and visualized. Not much cleaning was done; however, if I began to examine the years I would need to edit that column to only include the year. There were no null values. 

I did not remove any outliers from the data, nor did I transform or normalize the data in anyway. 

## Linear Regression Model Preparation and Creation

I evaluated how the features correlated with price as well as correlated with eachother. I picked 5 variables, which I believe had less of chance of colinearity. 

A training dataset for creating the linear regression model and a testing dataset was created by taking 80% of the data points for training and 20% for testing. 

The variables used in the linear regression model testing were sqft_living, grade, bathrooms, distance from epicenter, and waterfront. 










## Project Development
and my long-term goal is to include longitudinal data in order to predict a selling trend over time. With a longitudinal data set, I could also include tax appraisal in order to not only include the price of single-family homes, but also other buildings in the area. I would examine the borders of extremely valuable properties and considerably lower valued properties. I would want to identify the areas of highest value disparity within the closest proximity because these properties will most likely be bought by real estate developers in order to gain the maximum amount of profit. This typically happens in cities around the nation, and unfortunately this pattern of capitalism results in the displacement of many families who can no longer afford their rent. Since King County is developing at a rate faster than any other American city, the people who rent their homes are at a high risk of displacement. I would want to create a model that would pinpoint the areas most likely to be affected by gentrification over a ten-year span. Developers already work to pinpoint blocks that seem gentrifiable, which usually means buildings are in disrepair and are close to other gentrified areas. The rent gap is the disparity between how much a property is worth in its current state and how much it would be worth gentrified. The larger the gap in a neighborhood, the higher the chance it would gentrify. 

A rough equation to calculate the displacement risk may be:

 Number of nearby rich properties(mean tax appraisal of rich property) - Number of nearby poor properties(mean tax appraisal of cheap propert) 
 __________________________________________________________________
                         Distance
                         
The numerator of this expression should describe wealth disparity
 
 
 
