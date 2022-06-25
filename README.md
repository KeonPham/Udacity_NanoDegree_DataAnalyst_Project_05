# Ford GoBike System Data Exploration

## Dataset

The dataset is included 2,407,259 records of bike trips of BayWheel Sanfrancisco in 2019. 
After enriching features, the dataset has total 20 columns. There are one main category feature, that is `user_type` (Subscriber or Customer). 
We need to find the the pattern usage of different type of user for better understanding their behavior on different time dimensions.

## Summary of Findings
[Link to result: Part I Exploration Data Analysis](https://github.com/KeonPham/Udacity_NanoDegree_DataAnalyst_Project_05/blob/ded1c3515f23372535d48c243b0918cf2dea037b/Khoa%20Pham_Project%205_Part%20I_exploration.ipynb)
[Link to result: Part II Explanation Data Analysis](https://github.com/KeonPham/Udacity_NanoDegree_DataAnalyst_Project_05/blob/ded1c3515f23372535d48c243b0918cf2dea037b/Khoa%20Pham_Project%205_Part%20II_slide%20deck.ipynb)


This dataset has timing feature in full format (day, month, year & time). Therefore, we can enrich more features to this dataset by adding columns:
  - time of day
  - day of the week
  - day of month
  - month of the year
  - quarter_of_year
  - is_weekend

The trip duration in minutes is in such a wide range. Therefore, the I switch to use the log-scale for better visualization. It is skewed to the right. And it looks like unimodal distribution with the peak around 12 minutes.
Interestingly, there are 2 peaks in time of day 8am & 5pm. Most of the trip conducted.
There is a significant drop of trips on weekends compared to weekday.
82.5% of the trip is in weekday.
80.3% of the trip is from Subscribers.
There is a drop in trip in mid-month from every 13rd to 18th of the month
March & October are two months where the peaks are.
Seem the outliers of the dataset in duration is valid point. We consider to keep it for analysis.

Differnt user type interestingly has different behaviors based on the time dimensions. 
And this affect to the number of trip & trip duration over the time of them. 
The customers ride longer trip than subscribers almost double the average trip time. 
Seasonal factors has the affect on the number of trip and the trip duration as well esepcially the month of holiday season and in cold weather like January & February. 
The weekend is the time of riding in which the trip duration is higher than weekdays about 4-5 minutes. Depend of the time frame of the day, people has the different trip duration but the variation is bigger as the fewer number of trip taken. 
Based on the weekend or weekdays, the number of trip also has different patterns. The busiest time in weekday is on starting and finishing office working time. Whereas, weekend riders take the most of the trip on daytime.

Cusomter riders take longer trip in average than subscriber on every time dimensions. The seasonal factors indicates clearly on the heatmap over months on trip count and average trip duration of cutomers.



## Key Insights for Presentation


- 82.5% of trip is conducted on weekday rather than weekend. In addition, there are 80.38% of the trip is taken by subscriber than customer.
- Customer trip duration distribution is typically from 10 to 20 minutes that is longer than subscribers whose ride mostly is from 8 minutes to 10 minutes. And most of the customer is taking the longer trip which is longer than 50 minutes.
- Although the number of trips conducted by customer is smaller than subscriber, their average trip duration (22 minutes) is double from subscriber (11 minutes).  
- Average trip duration in 2019 is 13.41 min. The number of trips on Saturday & Sunday is lower compared to other days in weekdays. However, there is a big difference in the trip duration on weekends. People usually ride about 4-5 min longer than weekdays.
- Overall, the subscriber contributes the greatest number of the trip over the months of 2019. However, in December, trip count's customer is higher than subscriber. This could be because of the holiday season so our regular bikers are not going to commute to work (perhaps they take annual leaves) rather than the customer could be tourists or travelers from outside of the city.
- The month of using for subscriber is in March and April. After that the number of trips is dropping as coming to summertime and come back on springtime (September & October). And it significant dops on holiday season when most of office workers is taking time off from work and not commuting to work. On the other hand, customer starts using more bikes from September till end of the year. 
- On weekdays trips are mostly occurs on the time frame of commuting to work of office workers. As a result, most of the trip come from the subscriber. In contrast, on weekend, most of them is on daytime, so the trip absolutely come from the customer who perhaps use the bikes for explore the city or travelling to visit place for enjoyment.
- Customer rider has the average trip duration longer than the subscriber for the whole-time frame of the day and 7 days of the week.
- Customer focus their trip on the daytime of weekends. There is a significant average trip duration on early morning that could be the fewer number of trips taken during that time. The focus is on daytime from 10am till 6pm and on weekend to promote on weekend trip fun for the riders to getting to push the bike utilization on weekends.
- For Subscriber, almost the average trip duration is the same over the time of day and 7 days of the week. This could be different behavior from customer who could be tourists or travelers to spend more time on rides rather than office employees who commute to work and try to finish the trip as soon as possible.
- The seasonal factor has the effect on customer biker’s behavior on summertime (May, June & July) where the average trip on day of week of those months are denser from the rest of the month. This could be the season where people have the summer holiday and traveler will take the riders on those days. 
- The stable average trip duration of subscriber shows clearly on the heatmap over the weeks and months. They are expected to use the bike only for going to work.
- Average trip duration drops in December for both type of user.
- Most of the trip taken over the year of subscriber is on Monday to Friday and from January to November with the peaks Fridays of March, Tuesdays of April, and Tuesdays of October and the number significant drops in December. In contrast, the customer is getting hot in December from Monday till Friday. That is a bit surprising insight that we can customize the promoting and bike utilization based on the pattern usage of user type on different time dimensions.
