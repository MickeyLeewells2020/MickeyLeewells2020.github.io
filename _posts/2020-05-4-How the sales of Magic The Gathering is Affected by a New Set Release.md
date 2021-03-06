---
layout: post
title: How the sales of Magic The Gathering is Affected by a New Set Release

subtitle: Data exploration about my local gamestores sales  and drawing conclusions on correaltion about a new set release  MTG(Magic The Gathering)
gh-repo: MickeyLeewells2020/MickeyLeewells2020.github.io
gh-badge: [star, fork, follow]
tags: [Magic The Gathering,Data Science,Data Visualization]
bigimg: /img/mtg.png
comments: true
---


Initially I was doing a project based on whether or not Covid 19 had affected my local game store’s sales of Magic the gathering (MTG).
After looking at just a few graphs of my data set provided by the store, I came to the conclusion that was very obvious.
It was not affected to the degree that I had hoped, but by doing these exploratory analyses I did find a new question; What kind of effect does a new set release have on sales of MTG Singles and on the sales of a sealed product?
MTG singles are the single magic cards from when a store buys a card from a customer to sell later for a higher price. 
This customer would then get a store credit to use later to buy other cards. A sealed product is an unopened package that the store bought from the distributor to sell for a higher price. 
Unlike the single cards these are brand new and they have multiple cards in one package.
When I first got my data set from the store owner and uploaded the excel file to my Collab notebook.
It was a messed-up bunch of unnamed rows and columns. So, to start cleaning my data I dropped all columns that had NaN values or were unnamed.
NaN values are values that python does not recognize as a number. For example it would not recognize these characters: @, #, $, !.
I transposed the data set to use the same function that I used to drop the original columns to now drop as rows. 
Now that I had the dataset in the shape I wanted, I still needed to rename the columns as the datetime of the months for the data.
When that was done another problem had appeared. When I tried graphing it, I failed to check the type of variable python saw my data as.
Python was seeing it as an object. So, to correct the problem I had to coerce the object to become an integer value to be graphed correctly.

![weekl](/img/weekl.png)


This is a bar graph detailing weekly sales of MTG from October 2019 through April 2020. The blue bars are the sealed product sales and the red bars are the single card sales.
Originally the dataset for the monthly sales was all I had. I then requested more in-depth data from the owner.
The best he could manage was a weekly report.


![MTGbar](/img/MTG bar.png)


On January 18, 2020, there was the release of the new set “Theros Beyond Death”. 
There was a lot of hype around this release and many customers were excited to see the new cards.
As you can see in the graph January also had the most sales of sealed product.
In contrast ‘Throne of Eldraine ‘’was released on October 4, 2019. It was very average set release.
Now if we got take a look at the average of sealed product over the 27 weeks, the average is $983.
For context we take a look at the outlier, this would be the week of January 18, 2020. the sealed product sales were $3622 which is 268% more than the average. Also, for a comparison sale from the week of October 4, 2019 ‘Throne of Eldraine ‘’ had change from the average sales is 115% more than average. From this insight we can see that there is a pattern with a set release the week leading up to and a few weeks after depending on time of year will have increased sales.
[sources](https://magic.wizards.com/en/articles/archive/news/raising-new-banner-2017-10-08)
