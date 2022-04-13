# BSAN-6080-College-Ventures-Network


# Sprint 2 - Data Collection BSAN 6080


Robert Dryden <br />
Kyle Guillen <br />
David Rider <br />
Mfolozi Dlamini <br />
Jonathan Ting <br />



Tuesday April 12, 2022 <br />

### <ins>Data Collection Report</ins>

&emsp; Our first dataset is from our Facebook ads and shows the amount of clicks our website got per hour. 
Our goal with this project was to create a Facebook ad and then connect a pixel to our website with our ad in order to determine what kind of traffic our ad was generating. Unfortunately, this proved much more difficult than initially thought because of restrictions on the website we were working with. <br />
&emsp; Initially, we created our first version of our ad and began running it. This went smoothly and Facebook began providing key metrics such as interactions and website clicks from our ad. However, this data wouldn’t be enough to create a project around as they were simply key stats so we wanted to connect our data further and hopefully get a large sample of data. <br />
&emsp; Our next step was to look into integrating a Facebook pixel. The website we were working with (runtheworld) only had options for Facebook and Google pixels which is why we were not able to run our ads on Twitter. Thus began our attempt at creating a pixel from Facebook. There is an option to allow for a pixel with an ad and so we followed the instructions and placed the pixel in the integrations page of our runtheworld website. This would hopefully show us the traffic that was coming from our ad to the website. While this wouldn’t provide things such as click-through rates, it was an important first step in getting useful data. <br />
&emsp; However, what seemed like an easy first task proved difficult right away. The Facebook ad page is buggy and required multiple attempts at placing a pixel in order to effectively place it in our website. We were able to determine that our pixel was placed because we installed a Chrome extension that allowed us to see all the Facebook pixels on the website. We eventually saw our pixel and one other pixel (probably placed by runtheworld for all their websites) and began looking at how our Facebook ad worked with this. <br />
&emsp; The next portion of understanding the data had to be done through Facebook events manager. This, in theory, would show all the link clicks coming from our ad (as we had specified when creating our ad that we wanted to place a pixel from our ad) and would then allow us to connect other pages to find click-through rates. So, we decided to look into placing pixels on our other pages to find how they were performing. This would typically be done by going through the Facebook Events Manager section and inserting the website which you have your pixel on and adding other pages. However, Facebook said they couldn’t recognize our page as having the specified pixel. We determined this probably was an issue with Facebook because of multiple pixels being placed on the same website. <br />
&emsp; Thus, we were left with only being able to collect link-clicks from our specific ad to the main page of our website, or so we thought. As we were collecting our data, we noticed that in the Facebook ads section which highlighted key statistics of the ad, that the “link-clicks” number on that page was vastly different from that on Facebook Events Manager. It turns out that Facebook Events Manager was collecting general link clicks to our main page and was not following traffic generated from our  ad at all! Couple this with the fact that we had a timeline of two weeks for this data collection portion, a budget of $100, and had no access to any code on any of the websites we were running ads for, and you have a tough situation on your hands.<br />
&emsp; However, you might be thinking, “well there were certainly other options that could have been tested,” and you would be correct in thinking that. As runtheworld had an option for a Google Analytics pixel, we decided to venture into seeing if that was an option to find our extremely sought after click-through rates. <br />
&emsp; This was our first time using the Google Analytics platform, so there were initially some difficulties in placing the tracking tag, which was done using a “G-ID” identifier from a website property created within Google Analytics. Once we successfully placed that tag we began to see some usage data populating in the Google Analytics dashboard. I will briefly discuss the different types of data that is recorded and presented to us through Google Analytics. <br />
&emsp; The most basic form of information is simply the number of users on the website. This has slowly been increasing since the tracking began and has now reached 138 as of April 10th. The data becomes more interesting as we breakdown the sources of these users which Google Analytics labels as “first user source”. In this segment of the data we can see that a majority (113 / 138) of our users are coming from a “direct” source, while only a handful are coming from Google, Facebook, and also a CollegeVentures group chat. I did some further research into what was meant by a “direct” source, Google Analytics defines a direct user as website visits that occurred as a result of a user typing your URL directly into their browser or through bookmarks. So it seems like many of the users are either directly typing in the website name, or have it bookmarked. In addition to the website source of the user, Google Analytics also tracks from which country the user comes from. Most of which are United States, however there are a handful from Spain, Australia, and the UK. <br />
&emsp; The next interesting piece of information provided by Google Analytics is a tracking metric that they call “events”, this measures what the users do when they first get on the CollegeVentures website. These events include pageview (any user viewing the site), session start (which Google Analytics defines as any initial engagement to the site), first visits which tracks new users to the site, and lastly how many users scrolled on the site and how many clicked something. <br />
&emsp; These more detailed metrics, especially those relating to engagement such as scrolling and clicking, will provide us with an interesting way to define and measure the overall success of CollegeVentures event campaign. Combining this basic data from Google Analytics with the information gathered from the Facebook platform, we will hopefully have enough to generate a few surface level insights. <br />

###  <ins> Data Exploration Report </ins>
The data exploration report produces the result of running initial queries and visualization of the data we have collected. The main idea is to obtain a general understanding of the data we have collected and prepare our data for further analyses. In this report we will describe our first findings and their impact on the rest of the project. <br />

For the full report on the output as well as our graph visualizations please open the notebook titled **‘eda.ipynb’**. Please note that you will need to input **‘group3_data.xlsx’** as well **‘group3_analytics.xlsx’**. Both files are also included in the repository. <br />


###  <ins> Data Quality Report </ins>
For the quality of the data we ran into several problems.  The first being that when we generated our data reports, there were missing segments of data specifically around Day 0/1. This may have been due to the result of the advertising campaign taking longer to start up and therefore there wasn’t any engagement on the first days.  However, this will affect our end result because we won’t be able to determine engagement on a day to day basis from the days missing. 

Another problem with the data quality is that the data that we have on hand does not allow our team to make enough in-depth analysis and as mentioned previously, we are limited to using only surface level analysis on our project. 

Very broadly however, the dataset does answer the questions that needed to be answered.  It shows us the engagement of the users, location of some users, new user engagement, and website session directions.  However, the results of the data proved to be lackluster and much to be desired more than anything.   In regard to missing information we are missing platform conversions in our data quality report which can affect some options for analysis.

All in all, the quality of the data itself isn’t necessarily the primary problem.  The team ran into a multitude of problems running the campaign itself and it affected the results.  There was a lack of engagement and the amount of data we received was minimal.  The data that was collected unfortunately ends up being very surface level and we won’t be able to make any in-depth analysis. 

