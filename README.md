# PyBer_Analysis

## Overview

This analysis seeks to provide insight into ride accessibility and affordability for PyBer, a Python-based ride-sharing app company. Our goal is to perform exploratory data analysis on a large dataset to determine the relationship between the type of city, the number of drivers and riders, and the percentage of total fares, riders, and drivers by type of city. To achieve this goal, we would create several visualizations, write python scripts using pandas library and Matplotlib to create various charts. In the end, we hope to use the analysis and visualizations we produce to improve access to ride-sharing services and determine affordability for underserved neighborhoods.

After creating initial results, our analysis moves to a second phase where we make a summary DataFrame of the ride-sharing data by city type. Then, using Pandas and Matplotlib, we would create a multiple-line graph that shows the total weekly fares for each city type. Performing an exploratory analysis and creating visualizations using rideshare data to help improve access to rideshare services and determine affordability for underserved areas.

Finally, we would summarize how the data differs by city type and how decision-makers can use those differences at PyBer to answer questions around ride accessibility and affordability.

## Resources

•	Data Source: PyBer_Challenge_starter_code.ipynb 

•	Software: Matplotlib, Python 3.8.6, Visual Studio Code, Anaconda 4.8.6, Jupyter Notebook 6.1.4, Pandas

## Control Flow of Initial Analysis

1.	Import your data into a Pandas DataFrame.
	
2.	Inspect the data to determine the shape of the data, what types of columns are present, and if the data is readable or needs to be converted in some way.
	
3.	Merge your DataFrames.
	
4.	Create a bubble chart that showcases the average fare versus the total number of rides with bubble size based on the total number of drivers for each city type, including urban, suburban, and rural.
	
5.	Determine the mean, median, and mode for the following:

    - The total number of rides for each city type.
      
    - The average fares for each city type.

    - The total number of drivers for each city type.

6.	Create box-and-whisker plots that visualize each of the following to determine if there are any outliers:
	
     - The number of rides for each city type.

     - The fares for each city type.

     - The number of drivers for each city type.

7.	Create a pie chart that visualizes each of the following data for each city type:

     - The percent of total fares.

     - The percent of total rides.

     - The percent of total drivers.

## Deliverable 1: 

## A Ride-Sharing Summary DataFrame by City Type

### Results with detail analysis:

#### 1. The total number of rides for each city type is retrieved.

![image](https://user-images.githubusercontent.com/90879122/139614524-32fa36a8-eaa8-45a8-b9a8-a04a1f2494b6.png)

#### 2. The total number of drivers for each city type is retrieved.

![image](https://user-images.githubusercontent.com/90879122/139614571-c13e6d57-b056-408a-b6a0-25bc1f94d32b.png)

#### 3. The sum of the fares for each city type is retrieved.

![image](https://user-images.githubusercontent.com/90879122/139614667-2fa38d25-64d0-41ca-ac67-53ff5e7f3ea5.png)

#### 4. The average fare per ride for each city type is calculated.

![image](https://user-images.githubusercontent.com/90879122/139614708-00837852-d066-46bb-a7df-bd9b1a112286.png)

#### 5. The average fare per driver for each city type is calculated.

![image](https://user-images.githubusercontent.com/90879122/139614742-abf77398-150f-457c-8c06-151afc2c52a8.png)

#### 6. A PyBer summary DataFrame is created.

![image](https://user-images.githubusercontent.com/90879122/139614780-8b42235e-84ed-4e51-b377-c81900c0193d.png)

#### 7. The PyBer summary DataFrame is formatted as shown in the example.

![image](https://user-images.githubusercontent.com/90879122/139614809-b6584ed4-9fd4-40ca-bec9-8fa563aaaa2c.png)

## Deliverable 2: 

## A multiple-line chart of total fares for each city type

### Results with detail analysis:

#### 1. A DataFrame was created using the groupby() function on the "type" and "date" columns, and the sum() method is applied on the "fare" column to show the total fare amount for each date and time.

![image](https://user-images.githubusercontent.com/90879122/139614914-a76f8933-1c9d-4c16-94b8-518b9904bd6f.png)

#### 2. A DataFrame was created using the pivot() function where the index is the "date," the columns are the city "type," and the values are the "fare."

![image](https://user-images.githubusercontent.com/90879122/139614949-d0b9659b-2a95-4cde-8fe0-03a2ac0a7826.png)

#### 3. A DataFrame was created using the loc method on the date range: 2019-01-01 through 2019-04-28.

![image](https://user-images.githubusercontent.com/90879122/139615128-0ab403e9-2bae-4cca-9850-3bc5b8c62706.png)

#### 4. A DataFrame was created using the resample() function in weekly bins and shows the sum of the fares for each week.

![image](https://user-images.githubusercontent.com/90879122/139615161-0af5aa60-1208-4ba2-ba9e-39483586d9cc.png)

#### 5. An annotated chart showing the total fares by city type is created and saved to the "analysis" folder.

![image](https://user-images.githubusercontent.com/90879122/139615378-2109dbd3-5a83-40af-9a44-5e04708ef521.png)

## Results of the Initial and later Findings 

- 1.	In the initial findings the visual inspection of our bubble chart reveal that urban cities have the highest driver count and total number of rides, rural cities with the lowest number of rides and smallest driver count have the highest fares.

Note: Circle size correlates with driver count per city

![image](https://user-images.githubusercontent.com/90879122/139615664-cf2b5a3e-e0d1-4e5a-a6bd-e1b7ff0c9076.png)

- 2.	Our Summary Statistics for Number of Rides by City Type show that If we compare the average number of rides between each city type, we'll notice that the average number of rides in the rural cities is about 4 and 3.5 times lower than urban and suburban cities, respectively.

- 3.	Our Box and Whisker plot analysis reveals that There is one outlier in the urban ride count data. Also, the average number of rides in the rural cities is about 4- and 3.5-times lower per city than the urban and suburban cities, respectively.

- 4.	From our combined Ride fare data box-and-whisker plots, we see that there are no outliers. However, the average fare for rides in the rural cities is about $11 and $5 more per ride than the urban and suburban cities, respectively.

- 5.	 Why do you think there is such a big difference? 

  The number of drivers in rural cities helps explain this huge difference in fares, there are a smaller number of drivers compared to riders. Rural cities have a mean of 4    drivers and mean ride count of 7 {ratio 1:2} Urban cities have mean 24 ride count and mean 36 {ratio 2:3}; Suburban mean driver 14 and mean ride count 17 {ratio 4:5} Looking at the number of riders, we can suggest that Urban cities have the highest revenue.
  
- 6.	From our combined Driver Count data box-and-whisker plots, the average number of drivers in rural cities is nine to four times less per city than in urban and suburban cities, respectively. 

![image](https://user-images.githubusercontent.com/90879122/139615869-9a81f5c9-c73c-47c4-be0e-b50c3cff5346.png)


![image](https://user-images.githubusercontent.com/90879122/139615882-440034f3-1918-4b64-8de5-2001f6f23264.png)

Using the object-oriented interface method and the df.plot() method, as well as the Matplotlib "fivethirtyeight" graph style, we graphed the resampled DataFrame from the previous result to obtain to fares for the weekly bins in the following graph.

### Line Chart Showing Total Fares by City Type

![image](https://user-images.githubusercontent.com/90879122/139615945-348c73db-50f0-4aac-a557-ac8d2ba4cc3d.png)

# Summary

The PyBer Summary DataFrame provides an overview comparison of PyBer's ridesharing services in three types of cities: rural, surburban, and urban cities. The summary demonstrates that there is a larger demand for PyBer among riders in urban cities compared to suburban and rural cities. Between January 2019 and May 2019, there were 1,625 rides in urban cities, 625 rides in suburban cities, and 125 rides in rural cities. The figure below highlights how rides in Urban cities contributed the most to PyBer's overall rides during this five-month period.


#### Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types:

- 1) From our analysis, we can predict that there are good opportunities to expand the business in rural and suburban cities, including hiring drivers to operate and explode business in rural and suburban cities.

#### -  % of Total Drivers by City Type 

![image](https://user-images.githubusercontent.com/90879122/139616048-2620f8c9-f451-4d0b-a360-51469f7c54ba.png)

- 2) The Urban cities fare is the highest and consistent, giving us great and new business opportunities to expand rides.

#### - % of Total Fares by City Type

![image](https://user-images.githubusercontent.com/90879122/139616103-a7c0ce5f-d52f-420e-b362-8fa824dabf63.png)

- 3) The Rural cities fare is the lowest of the other two city types (Urban and Suburban cities), in addition, fares never intersect. Knowing that all fares never intersect, we can expand fares and increase business financial income to the company without affecting our rate.

#### - Total Fare by City Type 

![image](https://user-images.githubusercontent.com/90879122/139616204-19ef50a4-db6e-4c1a-966e-f96dd0c67687.png)





