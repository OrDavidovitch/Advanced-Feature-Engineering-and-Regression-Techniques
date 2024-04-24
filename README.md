# Advanced-Feature-Engineering-and-Regression-Techniques

My attempt at Kaggle's open competition for predictiong house prices.

We are given a training set with 1460 observations, each with a mix of some categorical and numerical features which sill help us predict the SalePrice of the house.
The objective is to try and predict the prices of the 1459 observations in the test set. 
We are measured using the RMSE between the log of our predictions and the log of the real price.

The main difficulty is trying to extract meaningful data out of the categorical features (about half of the original ~70 features are categorical) without increasing the dimension of the problem. This is dealt by transforming these features to ordinal ones using the rank sums test to detect significant difference between categories.

The next problem is avoidong multicollinearity between features. This is done by dropping some of the features with high linear correlation to others. We drop the ones with a weaker correlation to the target variable.

I tried multiple known and reliable regression models to tackle the problem. Each gave a descent result, but the beautiful result is that combining them into one using exponential weighting (with a uniform prior) gives us a great improvement to the best model we had.

In the repository you can find the Jupyter Notebook for the project and its pdf version, and all the test predictions for the different models as csv files.
