# A-B-testing-for-online-game


The aim of this work is to analyze dataset of A/B testing and after evaluation of the results provide with recommendation whether to launch or not to launch one or another version of variant. 
<br>

# Dataset
The dataset for this project can be found here: [Kaggle](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats). Download and load it.



# Objectives
* Present the goals, target metrics for each of A/B testings.
* Aggregate and prepare data as needed.
* Report key information about the A/B test, including calculations, statistical tests.
* Report the estimated treatment effect, confidence intervals and p-values.
* Compute the confidence interval both analytically and using bootstrap and report both intervals.
* Describe what calculations imply and which decision is recommended.
  
<br>


# Summary of A/B testing for Cookie Cats game
* Context: The goal was to find out what happends in terms of user's activity when the first gate in the game Cookie cats moved from level 30 to level 40. When a player installed the game, he/she was randomly assigned to either gate_30 or gate_40 and a few aspects were tracked: the number of game rounds played by the player during the first 14 days; did the player come back and play 1 day after installation or did the player come back and play 7 days after installation?
* Chosen metrics to evaluate versions were the proportion of users played more than 50 times, the proportion of come backs after 1 day, proportion of come backs after 7 day.
* During exploratory analysis it was noticed that samples were not equal, they were balanced by removing outliers and randomly sample users from the larger group to match the smaller group's size.
* Hypothesis were formulated based on these questions:
  1) Has other version was better than the old version by 2% in terms of the proportion of those who played more than 50 games?
  2) Has players' retention increased by 3% after 1 day?
  3) Has players' retention increased by 2% after 7 days?
* While answering question 1 it was assumed that samples sizes met the expected effect size to detect minimum effect, whereas for questions 2 and 3 sample sizes were recalculated by the expected effect.      
* Statistical Z tests were conducted for proportion comparisons on the chosen metrics.
* Analysis results implied that when considering version gate_40 vs version gate_30 in terms of the proportion of those who played more than 50 games, version gate_40 was better, a lift was 2.8%. However, when evaluating the percentage of retained customers after one or seven days, no differences between versions were detected.
* While making a decision to lauch or not to launch new version, costs of launching new version, business strategy (to increase the number of games played or make the same players to come back again and again), the way business earns money (i.e. advertisement before each game or money earned from subscribtion accounts of retained customers) must be considered and final decision should be tailored accordingly.

<br>
