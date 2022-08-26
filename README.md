# ML-House-Price-Prediction-Regression-Model

The objective of this model was to predict the prices of houses in a city.

I began by importing the data as Pandas DataFrame, and then I plotted the heatmap to find the number of NULL values in the data. I also saw the distribution of the data to identify whether the features are categorical or numerical, what is the mean of a feature, and how many unique values are there, etc.

Then I dropped the features with more than half the NULL values. Based on the unique values and number of Null values, I replaced the Null values with either mean or mode.

After dealing with the Null values, I replaced years with (2022-years) to get better relation with the Sale Price. I made a correlation matrix to identify which features are related too much to each other.

I plotted the relation of categorical features with the Sale Price using catplot to find the irrelevant features that did not have much impact on price and then dropped those features. For the remaining categorical variables, I created dummy variables and dropped the first one to remove the dependency.

After processing everything, I scaled the data (except y values) using Standard Scaler.

After splitting the data into an 80-20 ratio for training and testing, I fitted the Linear Regression and Random Forest model on the data and found that accuracy was higher for Random Forest.

I achieved an accuracy score of 0.87 which was further reduced to 0.75 after applying PCA and reducing the number of features to 18
