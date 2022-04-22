# bsan-6080-college-ventures-network

# BSAN-6080-College-Ventures-Network


# Sprint 3 - Data Collection BSAN 6080


Robert Dryden <br />
Kyle Guillen <br />
David Rider <br />
Mfolozi Dlamini <br />
Jonathan Ting <br />


Tuesday April 12, 2022 <br />

### Dataset Description
&emsp; Our data comprises of two main sources: our Facebook events data and our Google Analytics data. Our Facebook data is much less informative as it simply shows the amount of sessions our website got per hour. There are other key statistics that facebook has highlighted such as number of link clicks our ad got and the amount of impressions it got but it doesn’t show it as a time-series dataset. 
&emsp; Our other dataset comes from Google Analytics and has much more data we can use. In the data are number of visits, new users,  average engagement time, and trending users  per day on our website. It also has some other important datasets such as actions taken on our website and what countries our website was generating traffic from. 

### Rationale for Choice of Data
&emsp; First I will discuss the data that has been removed and why and then I will provide reasoning for keeping variables in our datasets. The first variable I removed from our data was user retention. This data was clearly not useful as there probably wasn’t enough traffic coming to our website to make valuable conclusions from this dataset. 
&emsp;The rest of the Google Analytics variables were not removed; however, we removed “server received count” and “total count” from our dataset as they provided no additional insights. Because “server received count” was always 0, it made “total count” equal to the “browser count,” therefore making those variables not necessary. 
&emsp; As data removal also has to deal with rows, it is important to note that no rows were removed from the datasets. As we can’t depict ad correlation too strongly, our main goal with our data is to showcase statistics and the trend of our website over a short period of time. The variables we have included: users, new users, avg engagement time, trending data, user sourcing data, country, session activity, and our facebook data will all allow us to create a variety of interesting visuals depicting our websites activity. 
It is important to note some limits of our data and clearly data volume is the largest one. It is hard to produce great insights with only 8 days worth of google analytics data so this was always going to be a potential limitation here. 

### Data Cleaning Report
&emsp; As there wasn’t a vast amount of data, there weren’t a lot of errors that needed to be cleaned up. The cleaning came in the form of putting all the data into one excel file. This was done through joining our datasets that could be joined together from our Google Analytics. We then renamed these sheets to have one conventional naming standard for them. Following this, the Facebook data was moved to the same file after removing the unnecessary variables previously discussed. 


###

attributes and records

Data Set: daily_data
Attributes: Day, users, new_users, avg_engangement_time, trending_30_d, trending_7_d, trending_1_d
Records: 0-8 (9 records)

Data Set: source_data
Attributes: ‘First user default channel grouping’, ‘New users’, Sessions
Records: Direct, Referral, Organic Social, Organic Search (4 records)

Data Set: country_data
Attributes: Country, Users
Records: United States, United Kingdom, Australia, Spain, India, Canada, Germany, Nigeria, Puerto Rico (9 records)
Data Set: session_data
Attributes: ‘Event name’, ‘Event count’
Records: page_view, session_start, first_visit, user_engagement, scroll, click (6 records)

Data Set: facebook_data
Attributes: unix_start_time, event, browser_received_count
Records: 3/31/22 17:00 -- 4/11/22 22:00  (150 records)



### Review of Process
&emsp; To be updated*

### List of Possible Next Steps
&emsp; To be updated*


#### Modeling

### Small Data: Simplistic Insights
Due to our difficulties in collecting data we were left with a very surface level set of information. This dataset does not lend itself to be used in any type of machine learning model or even simple linear regression. It is however better modeled using simple visualizations as well as some summary statistics. Our team has been able to create a number of different graphs and visuals to try to best illustrate our website tracking results. Additionally, in our "CLEANED_DATA_revised_2_%" I have added a basic summary metric to our session data. This percentage metric will serve as a proxy for a "funnel analysis" to give us a sense of what percentage of people who viewed the page completed a certain action. For instance 37% of users who viewed the page scrolled down to read it. This alone can be helpful in giving a sense for the success of the event's website.

In a scenario where we had complete access and design control over our own website, we could have generated a much richer dataset. That would also have given us the opportunity to run tests on our website design. If this test had been run we would have then been able to conduct statistical analyses to search for p-value significant differences in our A/B test design. We also could have generated a full user tracking funnel implemented in SQL.
