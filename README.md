# SF Crime Analysis and Modeling
****

## Project description
In this project, I investigate and analyze the crimes happended in San Francisco between Jan, 1st 2012 and May, 31st 2018. The target of this project is to analyze the trend and the distribution of crimes and give suggestions to police distribution and travelers.

Through this project, I learnt to build a data processing pipeline by Spark SQL and Spark DataFrame for big data Online Analytical Processing **(OLAP)**.
 
## Data Explore
### Crime count for different categories
<p align="center">
  <img width="600" height="400" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/1.crime_by_category.png">
</p>

Firstly, I explore the data by counting the crimes in different categories. I found most frequent crimes is theft

### Crime count for different district
<p align="center">
  <img width="500" height="400" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/2.crime_by_district.png">
</p>

Then, I count crimes happened in different districts. I found the top-3 dangerous districts are SOUTHERN, MISSION and NORTHERN. Thus, I think it's necessary to further investigate on these areas

### Crime count for different time

<p align="center">
  <img width="600" height="400" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/3.crime_by_time.png">
</p>

Due to the limited data, the crime happened in 2018 only recorded till May. So the crime counts happened in 2018 is much less than that in other years. 

From counting by different hours, I found that crime happens less frequently in the early morning, and more frequently at dinner time.

From counting by different day of week, I found cirme is more likely to happen during weekends.

### Trend of Crimes

Let's plot month count of crimes happened in 2015 to 2017.

<p align="center">
  <img width="600" height="400" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/4.trend_of_crimes.png">
</p>

### Analyze Crime on a certain day in recent 3 years

Let's take 12.15 as an example

<p align="center">
  <img width="400" height="400" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/5.day_analysis.png">
</p>


From above plots based on different time period, we can conclude that crimes happened in different time period has differnt counts.

Though 12:00AM~5:59AM has the least number of crimes happened, it unlikely for travelers to visit during that period.

So, I suggest travelers try to arrange their visiting in the morning and visit some indoor sites during afternoon to avoid crimes. 

### Crime analysis in top-3 danger districts

<p align="center">
  <img width="600" height="400" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/6.Mission.png">
</p>

<p align="center">
  <img width="600" height="400" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/6.Northern.png">
</p>

<p align="center">
  <img width="600" height="400" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/6.Southern.png">
</p>

Stolen is very likely to happen at these dangerous areas. Traveler should avoid traveling these areas between 16:00 -- 21:00. And if they travel to these areas, they shouldn't bring too many cash. 


### Violent Crime vs. Property Crime

<p align="center">
  <img width="500" height="300" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/7.%20Proerty_analysis.png">
</p>


For property crimes, we could observe that theft is increasing in recent years, vehicle theft had decreased to some extent. However, Burglary didn't decrease. Police department should think about possible solution for that


<p align="center">
  <img width="500" height="300" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/7.%20Violent_analysis.png">
</p>

For violent crimes, sex offense has noticably increased and we should inform these to the society so that citizens could learn some skills to proect themselves.


## Spatial analysis

Finally, I will do spatial analysis of crimes.

<p align="center">
  <img width="400" height="300" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/8.crime_shown.png">
</p>

I also run a kmeans clustering based on the spatial information of each crime. The cost vs. k plot is as following.

<p align="center">
  <img width="400" height="300" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/8.cost.png">
</p>

I chose k=15 as a choice between performance and computation complexity and then run k-means clustering again upon the data. 

<p align="center">
  <img width="400" height="300" src="https://github.com/butroy/SF_crime_analysis/blob/master/plots/8.kmeans.png">
</p>

Above is the reasul of 15-means clustering. I put a red triangle mark at the center of each area. I suggest police offices to allocate ther forces around the center area so that they could reach the crime at the fastest speed. 