# Predicting Wins in League of Legends at the 10 minute mark

## Goal

- This project aims to determine whether the blue team or the red team will win a game of league of legends at the 10 minute mark based on certain statistics about the game, including gold, kills, and experience (an in-game statistic, not how much experience the players have playing the game)
- The games are all from the diamond elo, which means that the players are some of the best players at the game

## Dataset

- The dataset was downloaded from Kaggle
- After removing features, the final dataset contained 9,879 observations and 32 features

## Feature selection 

- Features were removed based on covariance between features (if two features had a covariance of greater than .9, then one of the two features was removed)

## Models and results

- There were four models run:
	1) xgboost
	2) logistic regression
	3) random forest
	4) neural network
- Accuracy was chosen to determine which model performed the best
	- Since in theory both red and blue should win approximately the same number of games, approximately 1/2 of the results should be 1 and the other half should be 0, so using accuracy makes the most sense
- The logistic regression model performed the best

# Conclusion

- While it would be helpful to have more information about the champion's selected, it can still be approximated with nearly 3/4 accuracy which team will win based on statistics at the 10 minute mark of a high elo game