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

According to the PyBer summary dataframe, between January and May in 2019, there were 1,625 rides in urban cities, 625 rides in suburban cities, and 125 rides in rural areas. Also there were 2,405 drivers in urban cities, 490 drivers in suburban cities and 78 drivers in rural areas.

![](https://github.com/akthersr/PyBer_Analysis/blob/main/data%20summary.png)

The Urban city type had more total drivers than total rides, which had a dramatic impact on the average fare per ride and average fare per driver. The Urban drivers had the lowest average fare per ride and earned significantly less than the Rural drivers.
