# PyBer_Analysis

# Purpose

## The purpose of this analysis is to present a summary of ride-sharing data by city type using a dataframe and multiple-line graph. 

# Results

## For this analysis, two csv files were used. The ‘Ride Data’ file included data on city, date, fare and ride ID. The ‘City Data’ file included data on
city, driver count and city type. The files were merged to create one dataframe called ‘pyber_data_df’. 

To determine the total rides and fares by city type, the groupby() function and either count() or sum() function were applied to the merged dataframe.
Upon left merging the two data files, the driver count was distorted. As such, to calculate the number of total drivers, the groupby() and sum() 
functions were applied to the city_data dataframe. 

The average fare per ride was calculated by dividing total fares by city type by total rides by city type. The average fare per driver was calculated by
dividing total fares by city type by total drivers by city type. 

A new dataframe was created to summarize the results. 

IMAGE

The number of rides for urban cities was 1,625, approximately 2.5 times the number of rides for suburban cities and 13 times that for rural areas. 
However, total fares for urban cities was only 2 times that of suburban cities and 9 times that of rural cities. Accordingly, the average fare per ride 
was higher for rural cities at $34.62 as compared to $24.53 for urban cities and $30.97 for suburban cities. Additionally, the number of drivers in urban 
cities was approximately 5 times and 31 times larger than that in suburban and rural cities, respectively. Accordingly, the average fare per driver was 
significantly higher for rural cities at $55.49 as compared to $16.57 for urban cities and $39.50 for suburban cities. 

Further, using the loc() function, the data was filtered for dates between January 1, 2019 and April 29, 2019. Applying the resample() function, the data 
was distributed based on a weekly frequency and then plotted using df.plot().  

IMAGE

The line graph shows that for urban cities, total weekly fares ranged from approximately $1,600 to $2,500, with peaks occurring in late February and 
early March. For suburban cities, total weekly fares ranged between $700 and $1,500, with highest fares recorded in late February and again in late 
April. For rural cities, total weekly fares ranged from approximately $70 to $500, with highest total fares recorded in late February and early April. 

# Summary
The following are recommendations to address disparities amongst the city types: 
•	Review pricing of rides to determine appropriateness of fares. Total rides in urban cities were 2.5 and 13 times that of suburban and rural cities, respectively. However, total fares in urban cities were only 2 and 9 times that of suburban and rural cities, respectively.  
•	Include additional metrics, such as mileage per ride and fare per mile, to assist with pricing and profitability analysis. 
•	Review total number of drivers in each type of city to determine sufficient availability. In urban cities, total drivers exceed total rides by approximately 1.5 times. The opposite is true for rural cities, in which total rides exceeds total drivers.


