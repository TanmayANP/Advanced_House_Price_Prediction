# Advanced_House_Price_Prediction
* Build a ML model that takes the information of a house(in Ames, Iowa), predicts the selling price with an error of just $12700.
* Data is from the Kaggle **House Prices - Advanced Regression Techniques** competition.
* Did some Data Preprocessing (Outlier Detection, Handling Missing Values, Feature Engineering and remove skewness) on original data.
* Evaluated and optimized various ML models with cross-validation and graphs to reach the best model.
## Code and Resources Used
**Python version:** 3.8  
**Packages:** numpy, pandas, matplotlib, seaborn, scipy, scikit-learn, IPython.
**Dataset:** https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data  
## Data Description

https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data
For various categories in specific columns check the data_description.txt file.
Here we are given various features of .
## Data Cleaning
After, getting the data i needed to clean it up so that it was usable for my model. I made the following changes to our raw data:
*    Droped PassengerId column as it did not add any value
*    Droped Cabin and Ticket columns, these were categorical columns having too many categories in them with a chance of having new unseen categories in test data
## Data Preprocessing
Explained it in the project file.
## Model Performance
GradientBoosting model outperformed every other model on both test and validation dataset.  
*    **GradientBoosting Classifier** 79.88%
*    **Voting Classifier** 78.77%
*    **Logistic Regression:**  77.09%
*    **Support Vector Machine Classifier:** 77.09%
*    **RandomForest Classifier** 77.09%
*    **KNeighbors Classifier:** 75.41%
*    **ExtraTrees Classifier** 75.41%
*    **Adaptive Boosting Classifier** 74.86%
