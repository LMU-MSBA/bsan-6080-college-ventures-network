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


## Modeling

### Small Data: Simplistic Insights
Due to our difficulties in collecting data we were left with a very surface level set of information. This dataset does not lend itself to be used in any type of machine learning model or even simple linear regression. It is however better modeled using simple visualizations as well as some summary statistics. Our team has been able to create a number of different graphs and visuals to try to best illustrate our website tracking results. Additionally, in our "CLEANED_DATA_revised_2_%" I have added a basic summary metric to our session data. This percentage metric will serve as a proxy for a "funnel analysis" to give us a sense of what percentage of people who viewed the page completed a certain action. For instance 37% of users who viewed the page scrolled down to read it. This alone can be helpful in giving a sense for the success of the event's website.

In a scenario where we had complete access and design control over our own website, we could have generated a much richer dataset. That would also have given us the opportunity to run tests on our website design. If this test had been run we would have then been able to conduct statistical analyses to search for p-value significant differences in our A/B test design. We also could have generated a full user tracking funnel implemented in SQL.

### Models: Data Mining Goals 
Here is a revision of our Data Mining goals extracted from Sprint 1
Data Mining Goals are directly related to our main business goal
Business Goal: Assess the effectiveness of Facebook ads for increasing clickthrough rates and event RSVPs
Data Mining Goal translation: accurately track and visualize key performance indicators such as clickthrough funnel rate, average engagement, and number of event RSVPs
Determine Data Mining Success Criteria
We will be successful with this data mining goal if we are able to produce a user friendly dashboard which can be transferred over to the College Ventures Network social media team

Due to our limitation with our data we will describe the ideal Modeling that we would have completed a Logistic Regression to predict whether a person will attend the conference or not (0 or 1 binary). 
### Parameter Settings & Model Description
Model Technique: Logistic Regression
Use Case: To calculate or predict the probability of a binary (yes/no) event occurring. In this case to determine if a person is likely to attend the conference or not
Assumptions: As with any Logistic Regression Model our main assumption would've had to have been:<br/>
  - Independence of errors
  - Linearity in the logit for continuous variables
  - Absence of multicollinearity
  - Lack of strongly influential outliers.

### Generate Test Design
Test Design: The Logistic Regression would be implemented in python using individual web traffic data to our ad.

**Step 1:** Import the packages

**Step 2:** Read in the dataset. This would ideally be a single data row with the following features: age,start_time, end_time, page_view, session_start, first_visit, user_engagement, scroll, click, source, country, attend_conf
Data Dictionary Definitions:

age: numerical age of registrant
start_time: unix time user started the session
end_time: unix time user ended session
page_view: binary 1 or 0 (yes or no)
session_start: binary 1 or 0 (yes or no)
first_visit: binary 1 or 0 (yes or no)
user_engagement: binary 1 or 0 (yes or no)
scroll: binary 1 or 0 (yes or no)
click: binary 1 or 0 (yes or no)
country: numerical 0-195 countries
attend_conf: target variable binary 1 or 0 (yes or no)

**Step 3:** Exploratory Data Analysis


### Build Model
**Step 4:** Model building
Parameter Setting Model:
feature_cols = ['age','start_time', 'end_time', 'page_view', 'session_start', 'first_visit', 'user_engagement', 'scroll', 'click', 'source', 'country']
X= data[feature_cols]
y = data['attend_conf']




### Assessment (Data Mining Success Criteria)
**Step 5** Model Assessment

Revised Parameter Settings: Display the feature importance in order of decreasing influence on attending the conference or not

Perfomance Metrics:
- Accuracy
- Precision
- Recall
- Confusion Matrix
- ROC Curve
- AUC

For purposes of running our model we have opted to create a synthetic dataset to showcase how our model would run if had received the data we desired from Google Analytics or Facebook

The model is under the file **'synthetic_data.csv'** in our repository.

### Synthetic Model Performance Metrics
- Accuracy\
Accuracy: 0.64

- Precision\
Precision: 0.6666666666666666

- Recall\
Recall: 0.7142857142857143

- Confusion Matrix\
array([[ 6,  5],
       [ 4, 10]])
       
- ROC Curve (included in the ipynb notebook)\

- AUC\
Logistic Regression 0.66
