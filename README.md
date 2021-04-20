# tableau-challenge
Repository with my dashboard visualization created in Tableau Public.

Please see my visualizations published in Tableau Public by following the [link here.](https://public.tableau.com/profile/nadia2360#!/)

## Background
---
CitiBike provides data for each month in the form of CSV including such information as: 
* Trip Duration (seconds)
* Start Time and Date
* Stop Time and Date
* Start Station Name
* End Station Name
* Station ID
* Station Lat/Long
* Bike ID
* User Type (Customer = 24-hour pass or 3-day pass user; Subscriber = Annual Member)
* Gender (Zero=unknown; 1=male; 2=female)
* Year of Birth

For my analysis I have chosen to use the data for the following months: 
* March 2019
* March 2020
* March 2021

I wanted to specifically explore the difference in ridership between these months and years since that woudl show how Covid impacted the CitiBike program. I have uncovered some interesting trends that I'd love to share.

## Tools and Technology Used for Analysis
---
* CitiBike Data CSVs
* Python
* Jupyter Notebook
* Pandas
* Tableau

## Process Flow
---
1. CSVs into Pandas
2. Data munging
3. Data sampling
4. Uploading final CSVs to Tableau and creating visualizations and dashboards


## Data Limitations
---
During the cleaning process I have encountered some issues and came up with the following solutions (aside from normal data cleaning procedures:
1. The data for gender and birth year was not available for everyone, so rows with no value in those fields were dropped for my research purposes. However, if I was tasked with the main purpose of asessing the decline in ridership, I would have kept those values. My main purpose was to drill down into gender, age and user type, so that helped me to work with less data.
2. By seeing value counts I quickly realized that a preset year for those riders who have not entered their birth year was 1970. Although I realize that there may be a fair share of riders who were actually born in this year, I have dropped all the rows where birth year was 1970 in order to not get too skewed data on rider's birth year.
3. After visualizing this data, I believe data from April 2019, April 2020 and April 2021 would have been more telling to see how the ridership is growing during the pandemic aside from seeing the initial drop in April 2020. I did not have April 2021 data at the time of this research, so I chose to use data from the months of March over the 3 year span.
4. I have chosen to use a 5% sample of each resulted dataset (one for March 2019, March 2020 and March 2021) in order to visualize the data.


## Resulting Visualizations and Analysis
---
My exploration has resulted in 4 dashboards and 1 story from 15+ individual sheets.

### 1. Ridership By Gender and Age
Main takeaway from this visualization is to see how much ridership in general has dropped as compared to 2019. It is understandable why March of 202 is not yet showing such a decline as pandemic only started in the second half of March and people were not yet sure what to do till about April. I though what was facinating is the male/female ratio in 2021 vs 2019. When the riderhip dropped, it seems like both genders started to use it more equally. It may mean that either more males stopped riding CitiBike or the outreach to increase the number of female riders worked. Most likely, it is a combination of both, but that needs further exploration.
![Ridership By Gender and Age](https://github.com/nadiarichards/tableau-challenge/blob/main/Images/Ridership%20by%20Gender%20and%20Age.png)

### 2. Most Popular CitiBike Stations
This map shows all the CitiBike stations rated in size and color intesity based on popularity as a strt and end station. What was interesting to see is the change o=in popularity of the stations throught the pandemic. It may mean that people living in those neighborhoods were most likely to have moved out of the city at that time since most people start their trip on CitiBikes closes to their home. 

![Most Popular CitiBike Stations](https://github.com/nadiarichards/tableau-challenge/blob/main/Images/Most%20Popular%20CitiBike%20Stations.png)
![Most Popular CitiBike Stations by Year](https://github.com/nadiarichards/tableau-challenge/blob/main/Images/Most%20Popular%20Stations%20by%20Year.png)

### 3. Most Popular End Stations by Gender
I thought it was interesting to see that there is a big difference in popularity by gender specifucally for stations where peopel chose to end their trip. Top of mind for me was safety - or how safe women felt docking the bikes at those stations. I personally have a couple of CitiBike stations that I would rather not use as a female - for safety precautions.

![Most Popular End Stations for Men](https://github.com/nadiarichards/tableau-challenge/blob/main/Images/Most%20Popular%20End%20Stations%20for%20Men.png)

![Most Popular End Stations for Women](https://github.com/nadiarichards/tableau-challenge/blob/main/Images/Most%20Popular%20End%20Stations%20for%20Women.png)

### 4. Ridership and Trip Duration Breakdown by Gender
Here I wanted to see if trip duration differed a lot by gender, which it didn't. But, as mentioned before, male/female breakdown did change from March 2019 to March 2021 drastically. 

![Ridership Breakdown by Gender](https://github.com/nadiarichards/tableau-challenge/blob/main/Images/Male%20vs%20Female%20Ridership%20by%20Year.png)
![Trip Duration Breakdown by Gender](https://github.com/nadiarichards/tableau-challenge/blob/main/Images/Trip%20Duration%20and%20Time%20of%20Day%20by%20Gender.png)

### 5. Ridership by User Type
From this visualization one can easily tell that the decline in ridership from my first dashboard correlates with decline of subscribers to a CitiBike program. That is a veryy common situation for organizations that have a large subscriber base. Getting the subscriber amount back up is probably amoing the biggest challenges of CitiBike program right now.

![Ridership by User Type](https://github.com/nadiarichards/tableau-challenge/blob/main/Images/Ridership%20by%20User%20Type.png)

