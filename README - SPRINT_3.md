# bsan-6080-college-ventures-network

# BSAN-6080-College-Ventures-Network


# Sprint 2 - Data Collection BSAN 6080


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

### Review of Process
&emsp; To be updated*

### List of Possible Next Steps
&emsp; To be updated*


