# PyBer_Analysis
## Overview of the analysis
The main goal of this analysis is to provide ride sharing data visualizations for PyBer, a ride-sharing app company, inorder to improve access to rideshare services and determine affordability for underprivileged neighborhoods.The company provided all the rideshare data from January to early May of 2019, to analyze and create a compelling visualization for the CEO, V. Isualize.

## Resources
1.Data sources:city_data.csv,ride_data.csv.

2.Software: Python, Conda, Jupyter Notebook, Pandas.

3.Output files:PyBer_Challenge.ipynb,PyBer.ipynb.

## Purpose
The purpose of this analysis is to perform an exploratory analysis and creating visualizations using rideshare data,by PyBer.The PyBer Summary DataFrame provides an overview comparison of PyBer's ridesharing services in three types of cities and a multi-line graph of the total weekly fares for three city types: Rural, Suburban, and Urban.
## Analysis
The main steps are as follows:
1.With Pandas and Matplotlib library we can read the two csv files(city_data.csv,ride_data.csv).After merging the two data set,we count total rides,total drivers,total amount of fares,average fare per ride and average fare per driver.

![](https://github.com/akthersr/PyBer_Analysis/blob/main/total.png)

With the above metrices, a PyBer summary dataframe was created.

![](https://github.com/akthersr/PyBer_Analysis/blob/main/data%20summary.png)

Using the provided code snippet to remove the index name ("type") from the PyBer summary DataFrame,a formatted PyBer summary dataframe was created.

Then,we create a new DataFrame with multiple indices using the groupby() function on the "type" and "date" columns of the pyber_data_df DataFrame, then apply the sum() method on the "fare" column to show the total fare amount for each date.The dataframe as follows:

![](https://github.com/akthersr/PyBer_Analysis/blob/main/nan%20.png)

Using loc on the dates, a new dataframe was created for dates within '2019-01-01':'2019-04-28'.

We have to set the "date" index to datetime datatype and resampling the dataframe by week, a dataframe on weekly total fares by city type was created and visualized using a line graph.After resampling we get the follwing dataframe:

![](https://github.com/akthersr/PyBer_Analysis/blob/main/resampled.png)

## Results
### Summary DataFrame

By the PyBer summary dataframe, between January and May in 2019, there were 1,625 rides in urban cities, 625 rides in suburban cities, and 125 rides in rural areas. Also there were 2,405 drivers in urban cities, 490 drivers in suburban cities and 78 drivers in rural areas.The average number of drivers in rural cities is nine to four times less per city than in urban and suburban cities, respectively. By looking at the driver count data and fare data.Also, the average number of rides in the rural cities is about 4- and 3.5-times lower per city than the urban and suburban cities, respectively.

![](https://github.com/akthersr/PyBer_Analysis/blob/main/data%20summary.png)

The Urban city type had more total drivers than total rides, which had a impact on the average fare per ride and average fare per driver. The Urban drivers had the lowest average fare per ride which is $17 and earned significantly less than the Rural drivers.The average fare per driver is about $55 in rural cities, whereas the average fare per driver is about $17 in urban cities and Suburban cities' average fare per driver is about $40.The average fare per driver for suburban cities and rural areas are around 2.5 times and 3.5 times higher than urban cities, respectively.

### Total Fare by City Type
 
The below multiple-line chart "Total Fare by City Type" shows the PyBer Summary DataFrame by providing trends of total fares in rural, suburban, and urban cities between January 2019 and April 2019.

![](https://github.com/akthersr/PyBer_Analysis/blob/main/analysis/Pyber_fare_summary.png)

In the figure the yellow trend shows total fares in urban cities for Jan-April was about $1600 to $2400.The blue trend shows how fares in rural cities are around $300 from beginning to the end during the same period of time.The suburban trend fall in between rural and urban cities trend.At any given time,we see the total weekly fare of urban cities are higher than rural and suburban cities. As a result, Urban cities generate the most total revenue, compared to suburban and rural cities.For any types of city, a spike in total weekly fares can be seen in the third week of february.

## Summary 

Based on the results,we can provide the following three business recommendations to the CEO for addressing any disparities among the city types:
1. Instead of using only first third of the year,we can work with the whole year and provide insights into yearly trends.

2. In urban cities there are more drivers than the number of  total rides,so the urban drivers may not have enough work to support themselves.PyBer can promote some new offers to catch more customers and increase the total rides.This will reduce the fare price per ride and may increase availability of ridesharing services in these areas.

3. Discount can be offered to riders in rural and susburban cities to reduce fare per ride.As a result this may increase the ridership,total number of rides and drive down the fare per ride.We can also investigate the reason behind the the low volume of rides and total fares in rural and suburban cities.
  

