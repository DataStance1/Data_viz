#  Ford GoBike System Data Exploration 
## by Caleb Chijindu Ugorji


## Dataset

> This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area throughout the month of February 2019 and was obtained from https://www.fordgobike.com/system-data. Data consists of info about trips taken by service's members, their types, their age, their gender, stations of starting and ending trips, duration of trips etc.

### Preliminary wrangling
> There are 183412 observations and 16 columns in the dataset. Some columns contain null values. The station information columns contain 197 nulls while the member_birth_year column and the member_gender columns contain have 8265 nulls. The following columns have wrong data types - start_time, end_time, start_station_id, start_station_latitude, end_station_latitude, bike_id, member_birth_year, bike_share_for_all_trip. For analyses to go on, the null were dropped and the wrong data types corrected.
In order to carry out this analysis, some feautures like speed, distance, age, day_of_the_week, trip_kind were engineered


## Summary of Findings


> In the exploration, I found that there was a modest relationship between the trip duration and age of members, with modifying effect from gender,start day of trip and start hour. The distribution of the duration_sec and the distance had some unusual points. They were highly skewed to the right with long tails. However, after applying a logarithmic transformation to the plot, they followed a normal distribution.

### Some interesting findings
* The was a negative relationhip between trip duration and age. After the maximum trip duration, the trip duration declined with increase in age of riders
* The trip speed also declined with increase in age of the riders of the riders after the maximum speed
* There was an initial increase in the trip distance from age 20 to 30 then a decline in the distance as age increases from 30.
* Unexpectedly, the female gender has more longer rides than the other genders. They have a higher median duration_sec score than the other genders
* Though weekdays have more trips, users go for longer trips on saturday and Sundays(weekends).
* Males have higher median speed but the fastest trip was done by a female
* It has been established that we have more male users; a deeper look now reveals that a greater percentage of them are subscribers. This trend follows through all the genders.
* The female gender has more of the youngest users. Their median age is below that of the male and the other gender. The users in the Other gender are generally older with a median age higher than the female and male gender.
* Of the trips undergone by the male gender, short trips had the highest count followed by the intermediate trips, then long trips and finally very long trips. The female and the 'Other' gender, however, followed the reverse order with very_long trips as trips with the most count, followed by long trips, then intermediate trips and lastly, short trips. Their proportions also followed the same trend.
* The suscribers and the customers have roughly the same median age but the subscribers have a higher 75 percent quantile and higher max.
* Customers generally tend to go for trips with higher trip duration than subcribers. But the male gender in the customer level tends to have the highest trip duration while the male gender in the suscriber level tend to have the trips with the least duration.
* Trips with longer duration is embarked on mainly in weekends. Facetting trip_duration againt gender among the start days. The 'Other' gender tend to have more trips with longer duration than the male and female genders during the weekdays while during weekends, on saturday, the Male gender has the most trips with long durations and on sunday, the female gender has them.



## Key Insights for Presentation

> for the presentation, I focus on just on the factors that influence trips duration and leave out most of the intermediate derivations. I start by introducing the trip duration variable. followed by the pattern in age distribution, then plot the transformed scatterplot. Afterwards, I show the how gender affect trip duration, the pattern revealed by the data when average trip duration is plotted against member gender. I will also show how start day and start hour influence duration of trips using a polished vertical bar plot and a line plot
Finally, I will show how member gender relates with the categorical variable, trip kind.

