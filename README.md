# Advanced_House_Price_Prediction
* Build a ML model that takes the information of a house(in Ames, Iowa), predicts the selling price with an error of just $12700.
* Data is from the Kaggle **House Prices - Advanced Regression Techniques** competition.
* Did some Data Preprocessing (Outlier Detection, Handling Missing Values, Feature Engineering and remove skewness) on original data.
* Evaluated and optimized various ML models with cross-validation and graphs to reach the best model.
## Code and Resources Used
**Python version:** 3.8  
**Packages:** numpy, pandas, matplotlib, seaborn, scipy, scikit-learn, IPython  
**Dataset:** https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data  
## Data Description
We have the data of all the houses sold in the Ames, Iowa region between 2006 and 2010. The data set contains 2930 observations and various explanatory variables (23 nominal, 23 ordinal, 14 discrete, and 20 continuous) involved in assessing home values. For the categories in specific columns check the **data_description.txt** file. For further information on the data collection and preparation follow these links:-
https://ww2.amstat.org/publications/jse/v19n3/decock.pdf
https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data
## Data Cleaning
After, getting the data I needed to clean it up so that it was usable for my model. I made the following changes to our raw data:
*    Dropped rows with outliers in the Ground Living Area column
*    For those categorical columns having 'NA'(Not Available) or 'No' as categories, missing values have been replaced with 'NA' or 'No' respectively
*    For columns GarageArea, GarageCars, BasementFullBath, and BasementHalfBath, missing values have been replaced with 0
*    For instance, with no basement, numeric columns relating to the basement having missing value have been replaced with 0
*    Replaced missing values in the column LotFrontage using dictionary having medians of the LotFrontage grouped by the Neighborhood feature
*    Missing values in other columns have been replaced with the most frequently occurring value
## Feature Engineering
*    Some of the non-numeric predictors are stored as numbers; converted them into strings
*    Used column 'YearBuilt', 'YearRemodAdd', and 'GarageYrBlt' to create age feature of respective column
*    Created Total and Squared features of existing numeric features
*    Created some other intuitive features
## Model Performance
Tested various Linear models, Lasso Regressor outperforms all.
Here are the models used with their respective RMSE(Root Mean Squared Error) with cross-validation:-
*    **Lasso Regressor:** 0.1100
*    **Ridge Regressor:** 0.1143
*    **Stochastic Gradient Descent:**  0.1220
