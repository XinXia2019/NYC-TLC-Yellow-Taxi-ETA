## NYC TLC Yellow Taxi ETA

This project aims to apply machine learning models to predict taxi trip duration in New York City using TLC yellow taxi trips data in 2016 from Big Query.

## The major features we used:

`distance_in_km`: Haversine distance measures the shortest path distance between two points on the sphere. 

`avg_travel_time`: The average **historical** travel time in terms of the same *pickup area* and *drop-off area*, with geohash precision = 6. For example, if someone is traveling from abcdef (geohash code) to abcdeg (geohash code) at 15:00 on May 15th. The `avg_travel_time` will calculate the average travel time for trips that traveled from abcdef to abcdeg before May 15th 15:00. 

`avg_trip_dist`: The average **historical** trip distance in terms of the same *pickup area* and *drop-off area*, with geohash precision = 6. For example, if someone is traveling from abcdef (geohash code) to abcdeg (geohash code) at 15:00 on May 15th. The `avg_trip_dist` will calculate the average trip distance for trips that traveled from abcdef to abcdeg before May 15th 15:00. 

`kmeans`: Clustering similar trips based on pickup and drop-off location.

`visib`: Countinuous variable. The mean visibility for the day in miles.

`wdsp`: Continuous variable. The mean wind speed for the day in knots.

`temp`: Continuous variable. The mean temperature for the day in degrees Fahrenheit.

`fog`: Categorical variable. Indicators for the occurrence of fog during the day (1 = yes and 0 = no/not reported).

`rain_drizzle`: Categorical variable. Indicators for the occurrence of rain during the day (1 = yes and 0 = no/not reported).

`snow_ice_pellets`: Categorical variable. Indicators for the occurrence of snow during the day (1 = yes and 0 = no/not reported).

`week_index`: Categorical variable. Indicators for the weekdays and weekends (1 = Monday-Friday and 0 = Saturday-Sunday).

`rain_level`: Categorical variables. Indicators for the rain levels of the day. There are four levels including no rain, light rain, moderate rain, and heavy rain. There are 3 dummy variables in total for the rain_level feature.

`rush_hour_ind`: Categorical variable. Indicators for rush hour and off-peak hour in New York city (1 = 7-10AM, 3-7PM and 0 = the remaining hours).

