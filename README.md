# Background Story

![image](https://user-images.githubusercontent.com/94856154/154996331-b3b41f71-8e17-4302-afc8-09b0253173d9.png)
(Picture from Microsoft)

We've been hired by a mobile game company. Like most mobile games, this game has a store where players can buy a vast array of different items. Matches are composed of two players going head-to-head against each other. These two facts mean that there is a rich store of four tables:

As it is the game's one-year anniversary, my manager has asked me and one other team member to investigate player retention. Of specific interest is counting rolling 30-day retention and expressing it as a fraction of the total playerbase at the time. The tools we used are BigQuery and Google Sheets.

To address the question, we used the two following tables for our investigation:

1. Match information, including the players who matched against each other, and the outcome
2. Player information, including information like the player's age and when they joined

The SQL table should be including the folloing columns:
1. The day in question
2. The total number of players who joined that day
3. Of the players who joined, how many were retained
4. The fractional retention (the third column divided by the second column).



# Q1: Is 30-day rolling retention increasing or decreasing over the lifecycle of the game?
![Increasing or decreasing over the lifecycle of the game_](https://user-images.githubusercontent.com/94856154/155636714-af4473ef-619e-46f0-b7cc-c324c78c8896.png)

We excluded the last 30 days of the year from our analysis because those who joined in the last 30 days of the year would have automatically been categorized as Not-Retained. As the result, notibily, we saw a dramatically declined at the end of the year. Therefore, we only choose the data from Day 1 to Day 335 for this project.

By given the data above, we observed that from the trendline, overall the retention rate was quite consistent throughout the year(Average 65.46%). From a growth perspective, while the retention rate is stable in the trendline, the growth hasn't had significant increased since the Q1. There appear to be a few noticeable peaks in the retained player count (e.g. day 55 & 277), but it quickly adjusted back to the average line.




