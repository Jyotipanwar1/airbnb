# airbnb Listings
# Dataset Introduction
The selected dataset belongs to the in-depth details of Airbnb rental stays and the property description with stay feedback.This is a real time and true dataset. It does not contain synthetic additions.The records of stay in this dataset dates to December 2013 and has about 500,000 entries and 89 attributes in it including target variables such as daily price, weekly price and monthly .

# Problem Statement
The problem statement of this dataset is to predict daily prices for the upcoming future. This problem statement puts us in the domain of Sales Prediction.
The need of solving this problem statement is to maximize company profit and keep the customers happy at the same time.The sole revenue generation source of this company is to rent out other individual’s properties having empty living space available but no source to advertise it or real estate chains wanting to generate profit.The expected outcome is to maximize company (Airbnb) profit margin and best prices for Customer satisfaction.

# Approach
After exploring the dataset i concluded that, global dataset correlation of attributes with price (Target variable) is very weak thus we agreed to work on data of one country i.e. US.
After filtering records of US, we found correlation of attributes with our  target variable and manually picked numerical attributes out of 38 numerical attributes with moderate and above better correlations.Few attributes (e.g. Square feet) had more than 70% of missing values in it, which we dropped .We dropped null values from attributes which were negligible in count as compared to total data.It was found that our target variable is affected by various attributes but none have a considerably strong relationship. 
This is a global dataset as it has data of different countries.We have to filter out data and stick to one country in order to make data more useful.Entire dataset is skewed and has to be transformed/treated.Few datatypes were not relevant. Several missing values in dataset and also present in important attributes.

# Feature Selection
Once our EDA was done we moved on to model building where in selection of important features is necessary in order to make our model better.
SFS is also important in our data as we have 80 columns, which means a lot of redundant data.
SFS helps in eliminate unnecessary data.

# Model Building and Model Selection
There are different solutions to regression problems such as OLS, Regressor, Random forest, etc. and their metrics are:
OLS Model –  Significant R2 and Adj. R2 valuesIt suggested with 7 insignificant features
Regression  - Bettered OLS model with R2 value but larger RMSE, MAE as well. 
Decision Tree – Turned out to be the worst one with highest RMSE (0.77)
Random Forest Regressor – Best fit model with better R2 and reduced RMSE, MAE scores.
RMSE – 0.42, R2 – 72.98, Adj. R2 – 70.70
MAE – 0.27
Other methods and techniques such as PCA and XGBoost were tried but wasn’t much of use.
In this project, Random Forest Regressor turned out to be the best fit model for this problem as it reduced the RMSE to 0.52 and MAE -  0.27.


