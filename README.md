<font size="+3"><strong>Ford GoBike System Data Exploration</strong></font>

## Dataset


The data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area. It contains 16 features and well over 150,000 observations.
The Dataset is avaliable for download [here](https://video.udacity-data.com/topher/2020/October/5f91cf38_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv).


## Summary of Findings

In the exploration, I found that some features were having erroneous Data types, features "start_station_id","end_station_id" and "member_birth_year" was encoded as type floats instead of Int,  while  "start_time","end_time" were passed as string objects instead of a Datatime objects

Furthermore, I found that the feature, duration_sec has a very high positive skewed distribution which was almost diffcult to visualize but after removing the data points within the 10th and  90th quantile it was even easier to see the distribution of this feature.

Also, I discovered that the features "user_type", "member_gender" and "bike_share_for_all_trip" are highly Imbalanced in our Dataset.

As would be expected, I found a very strong positive correlation between features "start_station_latitude" and "end_station_latitude" and also between "start_station_longitude" and "end_station_longitude".


## Key Insights for Presentation

For the presentation, I focus on duration of trip [sec], Location of bike station [location columns], Days of the week, I engineered the feature "day of the week" from the Datetime column "start_time" to improve the quality of my exploration and leave out most of the intermediate derivations and wrangling.

I started by introducing the skewed distribution in the "duration_sec" variable and then move on to showing the distribution of member birth year and highlighting the year most bike riders in our dataset were born using a bar chart.

Moving on using color palette to show emphasis, I created a bar plot by exploiting the relationship between day of week and duration_sec to depict the day with the highest average time spent by the bike riders.

Finally, I created a scatter mapbox visualization using our location columns to show the locations of the bike stations on the map of San Francisco.

I chose this visulizations for presentation because they answer some of the initial questions I posed to myself when I was presented with this Dataset. 