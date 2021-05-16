---
layout: post
title:      "1st CLI Application "
date:       2021-05-16 23:32:01 +0000
permalink:  1st_cli_application
---


I started working on this application months ago. Like many, the hardest part was finding an idea and website that could help that idea. Of course I wanted to do something that was rare or did not exist. The other hard part is, working on a project part time. When your job takes you away for weeks at a time. Coming back and trying to pick up where you left off is time consuming. In this blow, I will highlight my path through my 1st application.

At the time that I started the project, covid has started coming down from the 3rd wave, early 2021. I am in the state of Arizona, and we were at one point, considered the hot spot of the world for positivity rate per capita. I was alway pretty interested in Covid. I was following it when there were just a few thousand cases in China, and predicted it would be here soon.

After learning so much about the virus, I discovered the biggest flaw in fighting the virus was testing. Many countries and many of the U.S states did not test adequately to combat the virus. For example, Arizona was very slow to start testing, and it gave our state a false sense of security, that infections in AZ were low. Clubs in Phoenix still were filled to capacity with no masks at NY and CA were still shut down.

I wanted to create an app that simply showed the daily testing count for each state.  It was easy to see how many positive cases we had, but not how many total tests were being done on a daily basis. To measure if a state is actually testing enough to get the real picture.

So I created an application that scrubbed data on covid testing. I searched for what seemed like weeks to find the right site that would be easy to scrub. There ended up only being a couple sites that provided the data I sought: Worldometer.info and CovidTracking.com. Worldometer.info by far is my favorite site for researching covid and other topics like population. Unfortunately, worldometer was incredibly difficult to scrape. I'm sure you can, but I struggled to figure it out. It is definitely a more advanced, layered website.

Covidtracking.com did exactly what I needed it to do. It gave me the totals for each states' daily covid count. It did not give the individual daily increase, that was going to be my applications' job.  It gave a graph on a different link, but you had to hover over each bar to see the amount. My app would be simple, all you had to do is type in your states' abbreviation and you have all the daily increase data for the state. For me, this is important because if testing was significantly down but the positivity rate was very high, the low positive case count could not give the full picture.

As far as the process for creating the application went, I felt it went pretty smoothly. Flatiron curriculum  definitely prepared me for the process. Especially the tutorials by Beth Schofield. 

Some points that I needed extra assistance on was the scraper. I tried a few different sites. I wasted a significant amount of time trying a chrome extension Chropath to do the scraping automatically.  After checking countless sites, I finally found a web page that did the trick and made my scraping much easier. The title for the site is not PG, reader discretion is advised. http://ruby.bastardsbook.com/chapters/html-parsing/. Then utilizing the ScraperChecker from GingerTonic, I was moving again.

Possibly the hardest part of the project was scraping one page, and needing to access multiple other pages from the site for each state to obtain the data. I was unable to create code that could snip 3 data points from each URL, so I hard coded each state's URL. That took some time, but the bulk of my time went into figuring out an enumerable method that could give me two items from the final element I will be using for my app. I tried select, find, and I could not get those to work. Somehow in my endless googling and forum scanning, I ran into .search. I found this site that showed me how to use it. https://www.algolia.com/doc/api-reference/api-methods/search/?client=ruby. This site is great because it shows how to use different methods with different languages. This allowed me to pull the text for the date and also the number of tests for that date.  Then I just had to create a method in the CLI class to subtract the previous date's count from the most recent date to give the daily tallies. 

This was a good experience for my first application. I would much rather be doing it full time so that I do not have to spend much time getting back into my flow, especially when this is brand new for me. I am excited to eventually start getting an app to work on a browser.







