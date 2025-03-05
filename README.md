# Overview
This project aims to answer the question: Can we predict a player's Slugging Percentage based on their Hits, Doubles, Triples, Home Runs, and At-Bats?

Data Sources:
- Los Angeles Dodgers batting data (LAD_batting.csv)
- Major League Baseball hitting data for 2023 (batting_2023_data.csv)

Libraries Used:
- Pandas (pd): For data manipulation and analysis.
- Scikit-learn (sklearn): For model training and evaluation (specifically train_test_split, RandomForestRegressor, and r2_score).
    - The train_test_split function is used to split data into training and testing sets
    - RandomForestRegressor is an ensemble learning method for regression tasks
    - r2_score calculates the coefficient of determination to evaluate model performance
- Matplotlib (matplotlib.pyplot): For creating visualizations.

Data Preparation:
- Relevant columns were selected from both datasets.
- Columns in the MLB dataset were renamed to match the Dodgers dataset.
- Slugging Percentage was calculated for the MLB dataset.
- Datasets were combined for analysis.

Exploratory Data Analysis:
A scatter plot of Hits vs Slugging Percentage was created to visualize the relationship between these variables.

Model Training:
- Features: Hits, Doubles, Triples, Home Runs, At-Bats
- Target: Slugging Percentage
- Model: Random Forest Regressor
- Train-Test Split: 80% training, 20% testing

Results:
The Random Forest model achieved an R-squared value of 0.9821, indicating that it explains 98.21% of the variance in Slugging Percentage.

Visualization:
A scatter plot of Predicted vs Actual Slugging Percentage was created to visualize the model's performance.

Conclusion:
The high R-squared value suggests that we can indeed predict a player's Slugging Percentage with high accuracy based on their Hits, Doubles, Triples, Home Runs, and At-Bats.

Limitations:
1. Data Scope: The analysis is limited to Dodgers data and MLB data from 2023, which may not represent all baseball scenarios or historical trends.
2. Feature Selection: Only basic batting statistics were used. Other factors like player position, ballpark effects, or opposing pitcher quality were not considered.
3. Overfitting Risk: The very high R-squared value might indicate potential overfitting, which could limit the model's generalizability to new, unseen data.
4. Temporal Limitations: The model doesn't account for changes in player performance over time or across different seasons.
5. Sample Size: The dataset size may not be large enough to capture all variability in baseball statistics.

Future Work:
1. Explore feature importance to understand which statistics contribute most to predicting Slugging Percentage.
2. Test the model on data from different seasons to assess its generalizability.
3. Consider incorporating additional features that might influence Slugging Percentage.

# ADD INFO ABOUT WHAT TYPE OF MACHINE LEARNING TECHNIQUE YOU USE AND WAS IT SUPERVISED OR UNSUPERVISED



# Project_2
Scatter plot of Hits vs Slugging Percentage:

This graph shows the relationship between the number of Hits a player has and their Slugging Percentage.

The x-axis represents the number of Hits.

The y-axis represents the Slugging Percentage.

Each point on the graph represents a player.

The scatter pattern can reveal if there's a correlation between Hits and Slugging Percentage.

We would expect to see a general upward trend, as more hits often contribute to a higher slugging percentage.

Any outliers or unusual patterns would be visible in this plot.


Predicted vs Actual Slugging Percentage. This visualization directly addresses our question of whether we can predict a player's Slugging Percentage based on their Hits, Doubles, Triples, Home Runs, and At-Bats.

Key features of this graph include:

X-axis: Represents the actual Slugging Percentage values from our test data.

Y-axis: Represents the predicted Slugging Percentage values from our model.

Scatter points: Each point represents a player, with their actual Slugging Percentage on the x-axis and the model's prediction on the y-axis.

Red dashed line: This diagonal line represents perfect predictions, where actual equals predicted.

The graph helps us interpret the model's performance in several ways:

Accuracy: Points close to the red dashed line indicate accurate predictions. The closer the points cluster around this line, the better the model's overall performance.

Over/under-prediction: Points above the line represent over-predictions, while points below represent under-predictions.

Spread: The vertical spread of points at any given x-value shows the range of predictions for similar actual values, indicating the model's consistency.

Patterns: Any visible patterns or clusters can reveal strengths or weaknesses in the model's predictions for certain ranges of Slugging Percentage.

This visualization complements the R-squared value by providing a detailed view of how well the model predicts Slugging Percentage across different actual values