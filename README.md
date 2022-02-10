# PyBer Analysis
## Overview of the analysis:
The purpose of Pyber analysis is to present business recommendations for CEO, V. Isualize. This analaysis and visualizations of ride-share data for PyBer to help improve access to ride-sharing services and determine affordability for underserved neighborhoods. Through the analysis, I wanted to see how the rides and fare data stack are affected by the average number of drivers for each city type. This will help V. Isualize make key decisions about where resources and support are needed.

## Analysis Results:
First of all, to create the summary of dataframe, I retrieval data and made group and count for each columns I need such as total rides, total driver and total fares. Once I know all the values of the list above, I calculated average fare per ride and average fare per driver by city type.

![Pyber_summary_DataFrame](https://github.com/msjj622/School_District_Analysis/blob/main/Images/replace_NaN_code%5D.png)

Second, by using two functions of pivot() and resample(), I created a multiple-line graph that shows the total fares for each week by city type. To create a new DataFrame with multiple indices, I firstly grouped on the "type" and "date" columns of the Pyber summary dataframe I created above. Then, used sum() method on the "fare" column to show the total fare amount for each date. 

![newDataFrame_type_date_fare](https://github.com/msjj622/School_District_Analysis/blob/main/Images/replace_NaN_code%5D.png)

I used the pivot() function to convert the DataFrame from the previous step so that the index is the "date," each column is a city "type," and the values are the "fare."

![newDataFrame_type_date_byCity_type](https://github.com/msjj622/School_District_Analysis/blob/main/Images/replace_NaN_code%5D.png)

After, using the dataframe by the function "resample()" and 'W' to get the sum of the fares for each week. You will see the result as the image below.

![newDataFrame_resample_w](https://github.com/msjj622/School_District_Analysis/blob/main/Images/replace_NaN_code%5D.png)


Finally, I created graph the resampled DataFrame from the dataframe above by using df.plot() method, as well as the Matplotlib "fivethirtyeight" graph style code. You will see the result by the image below.

![PyBer_fare_summary](https://github.com/msjj622/School_District_Analysis/blob/main/Images/replace_NaN_code%5D.png)

As you can see the line chart above, Urban city type has more afforability on fares and more demands comparing to other city type. It has more rides, more drivers. Although, the average fare per ride and driver is lower than other city type, the total fares are much higher.

## Analysis Summary: 
![PyBer_fare_summary](https://github.com/msjj622/School_District_Analysis/blob/main/Images/replace_NaN_code%5D.png)

As you can see the multiple-line chart above, the urban city type has more affordability which means it has more demends and the fare would be higher due to the high demands. For Pyber, a ride-sharing comany can have a good profit if we can focus on the services more in urban.

Other recommendations, in Rural area, Giving them discount for ride-sharing fares and see if they are willing to expend more. I think we have to know what would be reason that the residents in rural area wants to use ride-sharing serives to get more business ideas for the next steps.
