# Pyber_Analysis

Performing analysis on PyBer data for Module 5 challenge.

_Note: Chart Images below may not be completely visible in Dark Mode._

## Overview

PyBer, a python based ride-sharing app, has tasked us with analyzing all of the rideshare data from January to early May of 2019 and create compelling visualizations for the CEO, V. Isualize. The visualizations produced will showcase the relationship between the type of city (Urban, Suburban, and Rural) and the number of drivers & riders, as well as the percentage of total fares, riders, and drivers by type of city. The analysis will also include a summary DataFrame of the ride-sharing data by city type and a graph that showcases the total weekly fares for each city type. The analysis and visualizations will help PyBer improve access to ride-sharing services and determine the affordability for underserved neighborhood. 

To perform this exploratory analysis, we will be using Pandas libraries, matplotlib, and jupyter notebook. 

## Results

Two CSV files were analyzed and merged into a single DataFrame which contained the following information:
* City in which the ride took place
* Date & time of the ride
* Fare of the ride
* Ride ID number
* The number of Drivers in that city
* City Type (Urban, Suburban, or Rural)

The first relationship between ride-sharing data and city types can be seen in a scatter plot below. Each city type is represented by a different color bubble and its size corresponds to the number of drivers in that city. From this plot, we can see that Urban cities have the most number of rides per city and the highest driver count per city. Because of this, their average fare is the lowest. Inversely, Rural cities have the least number of rides per city with the lowest driver count. Because of this, the average fare in rural cities is the highest. Suburban cities fall in between.

![Fig1](https://user-images.githubusercontent.com/101564349/168471135-8b64f5b9-02d7-4e5d-8893-4ec65a87903f.png)

The next relationship is depicted via a box-and-whisker plot below. This plot visualizes the summary statistics and helps determine if there are any outliers in regard to the number of rides per city type. Looking at the plot, we can see that there is one outlier in the urban ride count data, plotted at 39 number of rides. Using the following code, we can decipher which city the outlier belongs to and thereby determine which city has the highest rider count.

``
urban_city_outlier = urban_ride_count[urban_ride_count==39].index[0]``

``
print(f"{urban_city_outlier} has the highest rider count.")
``

Our analysis tells us that the Urban city with the highest rider count is West Angela. We can also see that the average number of rides in rural cities is about 4 times lower than urban cities and approxiamtely 3.5 times lower than suburban cities. 

![Fig2](https://user-images.githubusercontent.com/101564349/168472326-c44cbca8-031e-450c-8b18-0f56549d229a.png)

The relationship between the number of drivers per city type can be viewed in the box-and-whisker plot below. In this plot, we can see that the average number of drivers in rural cities is approximately 9 times less per city than in Urban cities and approximately 4 times less per city than in suburban cities. 

![Fig4](https://user-images.githubusercontent.com/101564349/168474357-02f3c6c0-1101-4819-a40a-e4f907517031.png)

We can also view the relationship between the Fare per city type via a box-and-whisker plot. The plot below shows us that there are no outliers however, we can see that the average fare for rides in rural cities is around $11 more than urban cities and around $5 more than suburban cities. This can be due to the fact that there aren't as many drivers or rides in rural cities, and therefore it is more costly. 

![Fig3](https://user-images.githubusercontent.com/101564349/168473159-9c7dbc1a-5179-4c46-9ed9-4d49fbb17069.png)

Next, we can showcase the percentage of overall fares, percentage of rides, and percentage of the total drivers for each city type in pie charts. Each pie chart displays a consistent trend in which the percentages are highest for urban cities and lowest for rural cities, with suburban cities falling in between. From these pie charts, we can see that urban cities make up the majority of all fares for PyBer at 62.7%. This comes as no surprise as our analysis shows that Urban cities have the most drivers and rides at 80.9% and 68.4%, respectively. 

![Fig5](https://user-images.githubusercontent.com/101564349/168474754-a064ef85-73d8-44dd-a6ae-9410530c9f87.png)

![Fig6](https://user-images.githubusercontent.com/101564349/168474758-d61a180f-8d9c-4d9b-a124-a025e0bdc7d3.png)

![Fig7](https://user-images.githubusercontent.com/101564349/168474766-2d52e682-73c9-415a-abfb-2b37de2be335.png)


## Summary
