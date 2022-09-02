# Bike-Trip-Analysis

## Overview

This is an analysis and predictive model based on February 2019 Ford bike trip data from Kaggle.
Source: https://www.kaggle.com/code/nancyalaswad90/data-visualization-trip-data-ford-go-bike/data

Rideshares are becoming more and more popular in the US and the world. Although this is a limited dataset, are there any meaningful conclusions that can be drawn - 
  primarily, is there any predictive information that can be used to determine if and for how long a particular user will ride a bike, and from an operational standpoint,
  are there any bikes that see more use than others?

## Data

The dataset includes many variables, but the relevant ones to this project are: duration (seconds), bike id, user type (customer/subscriber), member birth year, member gender.

To better handle an understand the data, variables were created to represent time in minutes and hours. Categorical data - customer type, gender - were encoded to be represented numerically.

## Analysis

### Bike use frequency

![image](https://user-images.githubusercontent.com/72087263/187743810-25f1f3da-8725-4b25-ac75-97b6e0b3c5d7.png)


Bike id and duration (hours) were grouped by id and hours were summed. The resulting dataframe was plotted as a histogram to see if there were any differences. Values for quartiles and standard deviation were also calculated to better understand the data.

The majority of bikes were used for around 5 hours or less during the month of February. The third quartile and 90th percentile of bike usage were around 11 and 21 hours, respectively.

### Regression

A regression analysis was run using duration as the dependent variable and user type, gender, and age as the independent variables. The data was split into a training and testing set. The resulting model had an R2 of 0.013; hardly a useful model.

Plot of predicted vs true values:

![image](https://user-images.githubusercontent.com/72087263/188224774-9381a4d0-8f3d-4891-b743-f8cfbc08c83e.png)

To see if the model could be improved, a secon regression was run with five fold cross validation. This resulted in a marginally improve R2 of 0.014

Plot of cross validated predicted vs true values:

![image](https://user-images.githubusercontent.com/72087263/188225019-b143be2a-044a-4814-b24c-47588aaccbca.png)

To see if the model could be improved, a secon regression was run with five fold cross validation. This resulted in a marginally improve R2 of 0.014

## Conclusion

The results of this analysis show that from an operational standpoint, the operator could enact certain policies or procedures to ensure bikes are used at roughly similar rates. A more tailored maintenance schedule might also be adopted to reduce downtime for bikes.

The regression analysis failed to produce any meaningful results. I.e. from a marketing perspective, it is not possible to predict ride duration from variables including whether the user is a subcriber, user gender, or user age.
