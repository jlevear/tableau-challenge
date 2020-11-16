# tableau-challenge

### Analysis of Citi Bike data

The dataset I chose to look at is Citi Bike data from January 2019. The first phenomena I found was that Male rider had significantly more trips than Female riders and riders with Unknown gender. I decided to dive into this to see if I could find out more. 

## Gender Analysis

To begin, I decided to look at average trip duration for each gender to see if that could have an effect on the total trips. The average trip duration was around the same for each gender. Next I looked at median trip duration to see if there were any possible outliers and identify where the data was grouped. The median scores were around the same for each gender, and they were lower than the average. This told me that there were a greater number of shorter trips, and potentially some much longer ones that caused the average to be higher. This led me to look at the maximum trip duration for each gender. Again, they were around the same for each gender. The trip duration was measured in seconds, so the numbers I was looking at were very large. I decided I would convert the numbers to minutes, but the numbers were still too large, so I converted them to hours, and then again to days. The maximum trip durations turned out to be multiple days long, which I thought was interesting. Finally, I mapped the stations onto a map with circles corresponding to the number of trips by gender and combined it all into a dashboard.

The second phenomenon I wanted to look at was the number of riders with Unknown gender. There was a significant number, and I wanted to see if any other factors had in influence on this. I decided to look at rider age and see what I could find.

## Age Analysis

The first thing I did was make a map of each station with colored circles that corresponding to the median age. The median age was higher than I was expecting for each station at around late 30's. I expected the median age to be lower because I assumed that Citi Bikes used an app, which younger adults might be more comfortable using. Because of this, I made a simple bar graph showing the number of trips for each age. The graph looked more like I expected, with taller bars in the early-mid 20's, but there was also a strange spike for people aged 51 that was taller than all the other bars. This made me think that there was an individual or group of 51-year-olds that used Citi Bikes extremely often. I decided to check the maximum trip duration for each age to see if there was a similarity. However, the maximum trip duration was not evenly distributed and looked fairly random. And the 51 age bracked had the longest duration, but not by a lot.

In attempting to explain the large number of riders with Unknown gender, I had found another strange phenomenon, a large number of riders aged 51. To see if there was any relation between these two phenomena, I combined gender and age in my analysis.

## Gender and Age Analysis

I took the bar graph showing the number of trips by age and added gender as the color of the bars. I saw what I expected to see, a large portion of the bar with the Male color and a smaller portion with the Female color. However, the color for Unknown was not evenly distributed as I expected. For riders aged 51, more than half of the bar was Unknown, while for all other ages Unknown was a small sliver of the bar. It appeared that this was the reason for the spike in riders aged 51, since if we were to remove the Unknown portion of the bar, the bar would match the ones around it almost perfectly. 

I could not explain why the overwhelming majority of riders with Unknown gender were aged 51. Perhaps there is a default birth year that is selected if the customer declines to choose a gender or skips the question. I would recommend looking further into why this happened to improve data collection in the future.

## City Official Map

I was still interested in looking at ages when designing the Official City Map, so I added a map layer that showed the median age of the population based on zip code. I then added circle markers with their size corresponding to Citi Bike station popularity and their color corresponding to median rider age. I chose to use the same color scale for both the zip code map layer and station circles. This allowed me to compare the Citi Bike station median rider age to the zip code median age. 

As expected, the Citi Bike station median rider ages were slightly greater than the zip code median ages. I suspect this was due to the large number of riders recorded as aged 51, possibly in error, skewing the data.

## Further Research

Since New York City has a large number of tourists, I would be interested to know the percentage of the City Bike renters that were local. In order to gather this data, I would recommend capturing this information as part of the rental process. If renters are local, I would expect their demographics to match the demographics of the area in general (such as the census). It would be interesting to see where the demographics do not match. Knowing this might allow Citi Bike to target certain groups that do not currently use their service. 