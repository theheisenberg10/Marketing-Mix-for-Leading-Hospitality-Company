# Marketing-Mix-for-Leading-Hospitality-Company



## Reduced customer churn and boosted gaming ROI by 15%, delivering personalized marketing offers using Reinforcement Learning models adaptive to real time gaming behavior

## Evaluated impact of recommended promotions on net revenue leveraging statistical analysis and A/B tests

## Monitored Key Performance Metrics for business operations in real-time through interactive Tableau dashboards


## Business Problem - 
The main objective was to send personalized marketing offers (called free play in a casino setting) to players by observing data on their gaming behavior and demographic information. Since this was not a rudimentary prediction task, we opted to use reinforcement learning model here which learned what offer to send to each player so that the revenue from that player is maximized.

## Data 
We had data for player demographics, their gaming sessions, the offers(free play) sent previously to them. For our analysis we aggregated data on a player, offer level i.e. each row represented one offer sent to the player. We engineered some features based on the gaming behavior of the player like total money spent, total visits, revenue generated, etc. Now we had two types of data sources here for our project, static and dynamic variables. Static variables included the features of a player that did not change over time like demographics. Dynamic features that did change over time like total visits to casino, revenue generated till date, money spent on last visit, etc. After that we grouped the data further into player profiles instead of singular players so that our offers could be generalized to a group of players.

## Model 1 - Bayesian Regression
Then we trained a Bayesian regression model to predict the revenue generated within a month of sending the offer for each player. Our predictors included all the static and dynamic features and the amount of the free play offer. We used Bayesian regression instead of linear regression because for a player profile containing multiple players and for the same free play offer revenue generated could be a range of different values as the gaming behavior is different for different people. So, to capture this uncertainty we predicted a distribution of revenue instead of a single amount.

## Model 2 - Reinforcement Learning Multi Armed Bandit
Now that we got a distribution of revenue, we wanted to find out for each player profile out of all possible free play offers given, which offer is the best one i.e. which one would generate the most revenue. For this problem, we used the Multi Armed Bandit problem to model our solution. The MAB is a classic ML problem of a player who visits a casino but is not sure of what slot machine to play so that he can earn the most money. We just reversed the roles in our case and used it to solve our problem. We want to maximize revenue from the player but are not sure which free play offer to send.

	To solve this problem there are various approaches. We used the UCB algorithm to solve this which balances the exploration exploitation between free play values to maximize our revenue. The final output of our model was the free play offer on a player profile level. 
  
## Results
We managed to get a 15% boost in revenue from these personalized marketing offers compared to the older approach.
We also created Tableau dashboards for the marketing team to monitor real-time KP metrics from the players. One such dashboard showed how the Theo (profit generated from the player to the casino) varied over each session the player plays.

