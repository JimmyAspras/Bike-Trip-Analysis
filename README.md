# Bike-Trip-Analysis

Overview

This is an analysis and predictive model based on February 2019 Ford bike trip data from Kaggle.
Source: https://www.kaggle.com/code/nancyalaswad90/data-visualization-trip-data-ford-go-bike/data

Rideshares are becoming more and more popular in the US and the world. Although this is a limited dataset, are there any meaningful conclusions that can be drawn - 
  primarily, is there any predictive information that can be used to determine if and for how long a particular user will ride a bike, and from an operational standpoint,
  are there any bikes that see more use than others?

Data

The dataset includes many variables, but the relevant ones to this project are: duration (seconds), bike id, user type (customer/subscriber), member birth year, member gender.

To better handle an understand the data, variables were created to represent time in minutes and hours. Categorical data - customer type, gender - were encoded to be represented numerically.

Analysis

Bike use frequency

![image](https://user-images.githubusercontent.com/72087263/187743810-25f1f3da-8725-4b25-ac75-97b6e0b3c5d7.png)


Bike id and duration (hours) were grouped by id and hours were summed. The resulting dataframe was plotted as a histogram to see if there were any differences. Values for quartiles and standard deviation were also calculated to better understand the data.

The majority of bikes were used for around 5 hours or less during the month of February. The third quartile and 90th percentile of bike usage were around 11 and 21 hours, respectively.


Conclusion
