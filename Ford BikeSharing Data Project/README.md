# (Ford GoBike System Data Exploration)
## by (Emmanuel Udo)


## Dataset

>  This project is aimed at investigating how the number of trips and trip duration is dependent on other features (especially, user type) from the dataset. The dataset includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area in the month of February, 2019.

> The Data on each trip is anonymized and includes:
- Trip Duration (seconds)
- Start Time and Date
- End Time and Date
- Start Station ID
- Start Station Name
- Start Station Latitude
- Start Station Longitude
- End Station ID
- End Station Name
- End Station Latitude
- End Station Longitude
- Bike ID
- User Type (Subscriber or Customer where “Subscriber” = Member, “Customer” = Casual)

The wrangling steps taken:
- Data gathering
- Assessing data
- Cleaning data

Wrangling tasks completed in each of these steps are explained in the following paragraphs.

### 1. Data Gathering
> A single dataset was downloaded from a link provided on the provided udacity workspace

### 2. Assessing data
> After gathering, the dataset was assessed for tidiness and quality as follows:

> Dataset was visually assessed. A summary of the datatypes was also assesed. Then, IDs were checked for duplicates.

 > Dataset was assessed both visually and programmatically for the existence missing values, duplicate records and typographical errors at the point of entry

 > Critical decision was taken whether to remove NaN values from dataset immediately or not, if not now, what stage should be the perfect time to remove NaN values. Driving factor for this decision making was report accuracy. 

 > NaN values in the member_birth year column was later removed from the dataset only at one instance of exploration on riders age bracket. This happened at a much later part of the exploration project.
 
### 3. Cleaning data
> Quality and tidiness issues identified in the Assessing Data phase as underlisted below were cleaned using pandas:

> ### __Quality issues__

> 1. start_time, end_time columns has seconds in decimal places.
> 2. start_time, end_time columns has string datatypes, instead of datetime datatype.
> 3. start_time, end_time columns are not appropriately named.
> 4. duration_sec column is not appropriately named.

> __member_birth_year datatype will not be changed from float to integer till the later part of this project. This is because this column contains NaN values. Changing datatype here will require first removing the NaN values in this column which means row records with with these values will be dropped, thereby significantly reducing the number of rows/records of the entire dataset. This will negatively asffect the accuracy of the analysis.__

> ### __Tidiness issues__
> 1. Dataset contains features that are not necessary/useful for this project.


In-between these data cleaning tasks/operations, feature engineering was carried out to create columns that provide more datetime details and will probably be used for visualations later in the project.


## Summary of Findings

The following conclusions can be drawn from my analysis of the Ford GoBike Data System;
- Number of trips by riders is influenced by days of the week with most trips happening during the week days and fewer trips happening on weekends. Most of the trips were taken on Thursdays while Saturdays was the least. I plan on bringing this into my explanatory presentation.

- Number of trips by riders is also affected by the hours of the day as the number of riders is very low very early in the morning (12:00 AM) and drops further till 3:00 AM when it is lowest. The number of riders starts increasing from 4:00 AM till 8:00 AM. There is a considerable drop between 9:00AM and 10:00 AM. There is a relatively constant number of riders between the hours of 10:00 AM through to 2:00 PM. Another rise in trips is seen from 3:00 PM to 5:00 PM when the number of trips rises to its peak at 21,864 trips. And then finally, falls steadily till the midnight. 5:00 PM has the highest number of trips while 3:00 AM has the lowest number of trips. I plan on bringing this into my explanatory presentation.

- The number one trip start staion is Market St at 10th St while the least start staion is 16th St at Depot. I plan on bringing this into my explanatory presentation.

- Number of trips and average trip duration is also influenced by gender as riders are mostly male, then female. A few riders identify themselves as neither male nor female. I plan on bringing this into my explanatory presentation.

-  Bike rides is influenced by age bracket. Only a few riders are in their teens. We see an increase of riders in their twenties, with highest (most) riders in their thirties. Then we see a very significant drop as the riders approach their thirties. There is a further general drop as the riders age further. I plan on bringing this into my explanatory presentation.

- Summary of the relationship between trip duration and user types are as follows:
> 1. Customer user type has higher average trip duration (even higher than the maximum trip duration for subscribers) than subscriber. I plan on bringing this into my explanatory presentation.
> 2. Customers has higher average trip duration across the week from Mondays through to Sundays, than subscribers. I plan on bringing this into my explanatory presentation.


## Key Insights for Presentation

> Key Insights for my Presentation are as follows:
- Distribution of Trips across days of the week in the month of February, 2019 shows that number of trips by riders is influenced by days of the week with most trips happening during the week days and fewer trips happening on weekends.
- Distribution of Trips on hourly basis in the Month of February Year 2019 shows that 5:00 PM has the highest number of trips while 3:00 AM has the lowest number of trips
- Distribution of Riders by Gender shows riders are mostly male, then female. A few riders identify themselves as neither male nor female.
- Distribution of Riders by Age Bracket shows that, only a few riders are in their teens. We see an increase of riders in their twenties, with highest (most) riders in their thirties. Then we see a very significant drop as the riders approach their thirties. There is a further general drop as the riders age further.
- Average trip duration across the week by user type shows that customers has higher average trip duration across the week from Mondays through to Sundays, than subscribers.
- customer user type has higher maximum trip duration than subscribers
- Subscriber user type has lower minimum trip duration compared to customers
- Customer user type has higher average trip duration (even higher than the maximum trip duration for subscribers) than subscriber.