# bsan-6080-college-ventures-network


# Sprint 4 - Deployment BSAN 6080


Robert Dryden <br />
Kyle Guillen <br />
David Rider <br />
Mfolozi Dlamini <br />
Jonathan Ting <br />


Tuesday May 3, 2022 <br />


### Deployment Plan
Creating and maintaining a marketing information system (MIS) is a mission critical business process for today’s companies. A marketing information system is a process rather than a specific software platform and it guides the steps of a market driven company by collecting, coordinating, and analyzing all available marketing data. Insights gleaned from a robust marketing information system is important for providing relevant data to guide marketing plans, manage customers, and track marketing outcomes. While an MIS is not a software package much of the data collection, storage, and retrieval is completed with the help of a software platform. Many different software platforms are available and span the gamut from enterprise level software for Oracle and SAS to smaller systems using simply Microsoft Excel or MS Access. 

Having learned of the benefits of relational databases in previous coursework, we decided if we were to continue with this project we would implement our MIS with Microsoft Access since it is a relational database. Additionally, as Access is a part of the Microsoft suite it comes at no additional cost. Before setting up our database we complete a full analysis of the data that will need to be collected and write up a full requirements document.  Once the database had been fully modeled we would implement the database and start loading the data. As a next step we would seek to automate the database upload as part of an automated extract transform load (ETL) process. Data could be drawn from all relevant sources using APIs to transmit to our database. Our goal would be to keep the data in our MIS updated as rapidly as technically feasible. It is hoped that the ETL process would occur at least hourly if systems permit.  There are many companies that provide software specialized for the ETL process but in our plan we would plan to implement the process with some custom Python scripts and API calls that would run on an in-house server where jobs were scheduled through chron.

Once the automated ETL system has been put in place we plan to develop a marketing dashboard with all relevant  metrics as drawn from our database. Initially, we thought we might use Tableau to display the data since it offers advanced features, terrific graphics, and the ability to directly connect to a database. Another alternative would be to use Google Data Studio. Google Data Studio offers many of the same features as Tableau but is less sophisticated. However, if we started using Google Analytics extensively we might prefer function over form and go with Data Studio since it integrates exceptionally well with Analytics.  Our goal would be to develop different versions of the marketing dashboards depending upon the user. Top view and holistic data analysis would be provided to senior management and more granular details provided to analytics and marketing people for fine grained control of marketing decisions.


### Plan Monitoring and Maintenance



### Review Project
&emsp; This project taught us a lot of valuable skills that we hadn't yet acquired in the classroom. While it is great to practice the skills we already learned in our class such as data modelling and writing queries, our group enjoyed the troubleshooting aspect of this project, even if it didn't turn out exactly how we may have wanted. 

&emsp; First, there was working with Facebook ads. At the beginning of our project our initial hope was to work on Twitter ads so that we could use a system that was already in place and not have to create our own social media account. This quickly proved unsuccessful as we learned that the 3rd party who created the website (runtheworld.today) did not allow Twitter integrations. Thus, we started the process of not only creating our own account, but ur own ads to run. None of us had had any experience creating an ad and this was entirely new but even learning about things such as link placement within our ad and who to send our ads to was really interesting. After setting up our ad our next hurdle came in the form of placing a pixel on our website. This is something I believe Luis had talked about when he spoke and we touched on a little bit in class but I really had no idea of what this meant other than the conceptual idea of it. Getting to learn how these picels were placed and how to determimne if your pixel was actually placed was a really great exeperience. We also learned a lot about the process of tracking our ads and generating data from it. While, in the end we weren't about to come up with the CTR data that we would have liked, we were able to generate more ideas that could help us out.

&emsp; This is where Google analytics came in. Upon initial research, our goal was to get google analytics tracking code that could be placed to our website (through the integrations pane and not in the actual website HTML). However, we quickly determined that what we needed was a G-ID rather than code. Runtheworld only supported the ID and we found this out through trial and error (we tried emailing support but they didn't have a concrete example of what was supposed to go in that section). Eventually, the Google Analytics data started coming through and we were able to start tracking it. However, we were still unsuccessful in our attempts of finding CTR as working through the runtheworld website is quite difficult. 

&emsp; One thing we have truly learned from this project is how to deal with a bad project and inadqeuate data. For all of us, this was the least successful we have been in collecting data in any MSBA project. Learning how to handle error while still attempting to make something of it is a new skill most of us didn't want to have to learn on this project but came naturally. 

&emsp; As for our data mining process, a lot of work had to be done on the fly. Things like creating a synthetic dataset in order to showcase how our model would have worked helped us come to a good place in our project. Understanding the data we have and our limitations was a huge piece of this project for us when creating our models. While we may not have been able to come to a final conclusion with impactful insights, we were able to shwocase what we can do with such little data and how we can apply our skills with further data. 

&emsp; There are a few tips to be shared for different portions of the project. Firstly, when looking to run a project where data collected is through ads, make sure there is a way to easily track your CTR. We would recommend finding a company/website where the HTML can be accessed and code can be easily placed in. This will save a lot of hassle in trying to generate that without an easy setup. Second, if data collection looks unpromisiing, try to find other ways to acquire data. For example, we looked through Google Analytics and got data through there. Further, one could run tests on your ads to see if one ad performas better than the others. We tried this for our Facebook Ads but, seeing as we only had a 10 day window to run our ads and we were new to pixel placing, we only realized that we werent going to have a lot of data about 8 days in and this would have led to some really unbalanced A/B testing data. Lastly, when data is scarce, try to make the most out of what you have. Things like feature engineering from dates or trying to create more variables from what you have can be really helpful in coming to some sort of conclusion later on. 
