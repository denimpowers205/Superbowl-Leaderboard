# Superbowl-Leaderboard
 “Does the position of the Super Bowl MVP help predict the point difference in the Super Bowl?”  Sub Question: The purpose of seeing if QB MVPs happen in closer games or if defensive MVPs happen in blowouts.


This project aims to answer the question: 'Does the position of the Super Bowl MVP help predict the point difference in the Super Bowl?' with a specific focus on whether Quarterback MVPs occur in closer games or if defensive MVPs are associated with blowouts.

Here's a description of the project:

Project Title: Super Bowl MVP Position and Point Difference Analysis

Objective: To investigate the relationship between the position of the Super Bowl Most Valuable Player (MVP) and the point difference in the Super Bowl game.

Methodology:

Data Loading and Preparation: The project begins by loading the SuperBowl_History.300 - SuperBowl_History.csv dataset into a pandas DataFrame. Initial data preparation involves:
Calculating the point_difference between the winning and losing teams.
Extracting MVP position information to create boolean columns for Offense and Deffense MVP types.
(Note: A HoF column was created but not explicitly used in the main analysis presented).
Exploratory Data Analysis (EDA): Box plots are generated to visualize the distribution of point differences for both Offensive and Defensive MVPs. This visual analysis is complemented by calculating and comparing the mean point differences for each MVP type.
Findings from EDA: The analysis suggests that:
Offensive MVPs tend to occur in games with lower point differences, with a median closer to 10 points.
Defensive MVPs are generally associated with games having higher point differences, with their interquartile range being notably higher than that of offensive MVPs. The mean point difference for Defensive MVPs (19.56) is significantly higher than for Offensive MVPs (12.48).
The conclusion drawn is that defensive MVPs are more likely to happen in games with larger score differentials.
Predictive Modeling (K-Nearest Neighbors): A K-Nearest Neighbors (KNeighborsClassifier) model is used to predict the MVP type (Offensive or Defensive) based on the point difference. The model is trained on resampled data and evaluated using a confusion matrix and performance metrics (accuracy, precision, recall, F1-score).
Conclusion from Modeling: The model correctly identifies 9 offensive MVPs and 2 defensive MVPs. However, it misclassified 6 offensive MVPs as defensive MVPs, indicating an overlap in point differences between the two MVP types, particularly for closer games, which makes prediction challenging. The overall accuracy of the resampled model is 0.6111.

Overall Project Insight: The project successfully demonstrates a discernible pattern: Super Bowls with Offensive MVPs generally exhibit smaller point differentials, while those with Defensive MVPs tend to have larger point differentials. However, the overlap in point difference distributions indicates that point difference alone is not a perfect predictor of MVP type.

