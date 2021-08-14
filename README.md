# Air-Quality-Index
# It collects the weather data from multiple web sites , combines and process the training data and creates various ml models to predict the Air-Quality-Index based on other features like Max and Min Temp, Humidity etc.

# Data Collection 1

Collecting the data from https://en.tutiempo.net/climate,using Html_script.py.

This site contains climate data like Average Temp, Max Temp,Min Temp,Humidity,Visibility, Wind Speed etc except the AQI value, which is the Dependant Feature.

This data is stored in a tabular format month-wise.

It is extracting the climate data of New Delhi from 2013 to 2019 month-wise.

Html_script.py will create year-wise folders and store 12 html files for 12 months each, for the same year.


# Data Collection 2

AQI value which is termed as PM2.5, i.e Particulate Matter which is a mixture of solid and liquid particles that are suspended in the air.

This data is collected from wheathermap.com.

AQI_data folder contains the PM2.5 data from 2013-2019.

The is in Date-wise, hour-wise format, we need to match it with the climate data which is in day-wise format.

Plot_AQI.ipynb is the code for cleaning the AQI_data and return the average PM2.5 of hourly data for a particular day.

# Data Preprocessing

Extract_combine.ipynb is used to combine climate data from Data Collection 1 and PM2.5 data from Data Collection 2.

This code have 2 methonds viz. met_data() which uses beautifulsoup to extract the data elements, which are my dependant features, from html files and data_combine() is to add 

PM2.5 for each year,which are my dependant features.

Real_combine.csv is my final dataset which combines all year's data in a single csv file.

# Training

I have used the following models on the dataset to compare the best performing models.

1. Linear Regression
2. Lasso Regression
3. RandomForestRegression
4. Xgboost Regression
5. Decision Tree
6. Artificial Neural Network








