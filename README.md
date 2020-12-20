# Sales-Forecasting
Sales Forecasting using Machine Learning Techniques
<br/>
<br/>
# Kaggle Folder
The Kaggle folder contains the input dataset
<br/>
# Predicted Data Folder
Contains ***submission.csv*** which has all the predicted data after training the model
<br/>
# savedModels.json
A JSON file which contains the link of the Random Forest Regression Model that we trained and saved. The Model is 1.22 GB and hence was linked instead of directly being uploaded on GitHub.
<br/>
# Sales Forecasting Machine Learning.ipynb
### This NoteBook contains all the code for Data Analysis, Training, Tuning and Testing in a proper order.
<br/>

## Data Set Description
### stores.csv
This file contains anonymized information about the 45 stores, indicating the type and size of store.
### train.csv
This is the historical training data, which covers 2010-02-05 to 2012-11-01. Within this file you will find the following fields:
* Store - the store number
* Dept - the department number
* Date - the week
* Weekly_Sales -  sales for the given department in the given store
* IsHoliday - whether the week is a special holiday week
### test.csv
This file is identical to train.csv, except we have withheld the weekly sales. You must predict the sales for each triplet of store, department, and date in this file.
### features.csv
This file contains additional data related to the store, department, and regional activity for the given dates. It contains the following fields:
Store - the store number
* **Date** - the week
* **Temperature** - average temperature in the region
* **Fuel_Price** - cost of fuel in the region
* **MarkDown1-5** - anonymized data related to promotional markdowns that Walmart is running. MarkDown data is only available after Nov 2011, and is not available for all stores all the time. Any missing value is marked with an NA.
* **CPI** - the consumer price index
* **Unemployment** - the unemployment rate
* **IsHoliday** - whether the week is a special holiday week

For convenience, the four holidays fall within the following weeks in the dataset (not all holidays are in the data):
* **Super Bowl**: 12-Feb-10, 11-Feb-11, 10-Feb-12, 8-Feb-13
* **Labor Day**: 10-Sep-10, 9-Sep-11, 7-Sep-12, 6-Sep-13
* **Thanksgiving**: 26-Nov-10, 25-Nov-11, 23-Nov-12, 29-Nov-13
* **Christmas**: 31-Dec-10, 30-Dec-11, 28-Dec-12, 27-Dec-13

## Weighted Mean Absolute Error
The models would be evaluated on the weighted mean absolute error (WMAE):\
<img src="https://latex.codecogs.com/gif.latex?\huge&space;WMAE&space;=&space;\frac{1}{\sum&space;w_{i}}\sum_{i=1}^{n}w_{i}\left&space;|&space;y_{i}&space;-&space;\widehat{y_{i}}&space;\right&space;|" title="\huge WMAE = \frac{1}{\sum w_{i}}\sum_{i=1}^{n}w_{i}\left | y_{i} - \widehat{y_{i}} \right |" />
