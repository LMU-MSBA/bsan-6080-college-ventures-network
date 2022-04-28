# bsan-6080-college-ventures-network


# Sprint 4 - Deployment BSAN 6080


Robert Dryden <br />
Kyle Guillen <br />
David Rider <br />
Mfolozi Dlamini <br />
Jonathan Ting <br />


Tuesday May 3, 2022 <br />


### Deployment Plan


### Plan Monitoring and Maintenance



### Review Project
&emsp; This project taught us a lot of valuable skills that we hadn't yet acquired in the classroom. While it is great to practice the skills we already learned in our class such as data modelling and writing queries, our group enjoyed the troubleshooting aspect of this project, even if it didn't turn out exactly how we may have wanted. 
&emsp; First, there was working with Facebook ads. At the beginning of our project our initial hope was to work on Twitter ads so that we could use a system that was already in place and not have to create our own social media account. This quickly proved unsuccessful as we learned that the 3rd party who created the website (runtheworld.today) did not allow Twitter integrations. Thus, we started the process of not only creating our own account, but ur own ads to run. None of us had had any experience creating an ad and this was entirely new but even learning about things such as link placement within our ad and who to send our ads to was really interesting. After setting up our ad our next hurdle came in the form of placing a pixel on our website. This is something I believe Luis had talked about when he spoke and we touched on a little bit in class but I really had no idea of what this meant other than the conceptual idea of it. Getting to learn how these picels were placed and how to determimne if your pixel was actually placed was a really great exeperience. We also learned a lot about the process of tracking our ads and generating data from it. While, in the end we weren't about to come up with the CTR data that we would have liked, we were able to generate more ideas that could help us out.
&emsp; This is where Google analytics came in. Upon initial research, our goal was to get google analytics tracking code that could be placed to our website (through the integrations pane and not in the actual website HTML). However, we quickly determined that what we needed was a G-ID rather than code. Runtheworld only supported the ID and we found this out through trial and error (we tried emailing support but they didn't have a concrete example of what was supposed to go in that section). Eventually, the Google Analytics data started coming through and we were able to start tracking it. However, we were still unsuccessful in our attempts of finding CTR as working through the runtheworld website is quite difficult. 
&emsp; One thing we have truly learned from this project is how to deal with a bad project and inadqeuate data. For all of us, this was the least successful we have been in collecting data in any MSBA project. Learning how to handle error while still attempting to make something of it is a new skill most of us didn't want to have to learn on this project but came naturally. 
&emsp; As for our data mining process, a lot of work had to be done on the fly. Things like creating a synthetic dataset in order to showcase how our model would have worked helped us come to a good place in our project. Understanding the data we have and our limitations was a huge piece of this project for us when creating our models. While we may not have been able to come to a final conclusion with impactful insights, we were able to shwocase what we can do with such little data and how we can apply our skills with further data. 
&emsp; There are a few tips to be shared for different portions of the project. Firstly, when looking to run a project where data collected is through ads, make sure there is a way to easily track your CTR. We would recommend finding a company/website where the HTML can be accessed and code can be easily placed in. This will save a lot of hassle in trying to generate that without an easy setup. Second, if data collection looks unpromisiing, try to find other ways to acquire data. For example, we looked through Google Analytics and got data through there. Further, one could run tests on your ads to see if one ad performas better than the others. We tried this for our Facebook Ads but, seeing as we only had a 10 day window to run our ads and we were new to pixel placing, we only realized that we werent going to have a lot of data about 8 days in and this would have led to some really unbalanced A/B testing data. Lastly, when data is scarce, try to make the most out of what you have. Things like feature engineering from dates or trying to create more variables from what you have can be really helpful in coming to some sort of conclusion later on. 
