# Using Regression Analysis to predict California Housing Prices 
The dataset for California housing price is taken from the StatLib library and is maintained by the Computational and Applied Mathematics Group at UC Berkeley. The dataset contains information on the housing prices in California, including features such as the population, total number of rooms ,total number of bedrooms ,housing median age, longitude and latitude.

**Dataset: [https://www.kaggle.com/datasets/camnugent/california-housing-prices](https://www.kaggle.com/datasets/camnugent/california-housing-prices)**

## Data Description

The California Housing Prices Dataset contains 9 variables and 20,640 observations:

1.  **population:** a float value indicating the population in the area
    
2. **total_rooms:** a float value indicating the total number of rooms in the area
    
3. **total_bedrooms:** a float value indicating the total number of bedrooms in the area
    
4. **housing_median_age:** a float value indicating the median age of the housing in the area
    
5. **households:** a float value indicating the number of households in the area
    
6. **median_income:** a float value indicating the median income of the area
    
7. **median_house_value:** a float value indicating the median house value in the area
    
8. **longitude:** a float value indicating the longitude of the housing area 
    

9. **latitude:** a float value indicating the latitude of the housing area

## Usage

This dataset can be used for a variety of tasks, such as data exploration and visualization, feature engineering,regression analysis, and more. So, i build models that predict housing prices based on various features and can provide insights into the relationships between various demographic factors and housing prices .

## Methodology

1.  I imported all the necessary libraries into our project.
    
2.  I load the dataset.
    
3. I checked the columns and their data types.
    
4.  I found the ocean_proximity column as an object.
    
5.  I checked for null values in our dataset. i found 207 null values in the bedrooms column.
    
6.  I replaced the null bedroom values with room values. Now there are no null values left in the dataframe.
    
7.  I encoded the ocean proximity column.
    
8.  I checked the correlation heatmap for our dataframe.
    
9.  I checked the median house value column distribution of our dataframe.
    
10.  I splitted my data into train and test respectively 80/20 splits.
    
11.  I trained Linear Regression, XGBoost and Catboost for our dataframe.
    
12.  In linear regression i got 0.6298 as R2 score and 0.3058 as MAPE (Mean Absolute Percentage Error). Then i plotted the model for evaluation .
    
13.  In XGBoost i got -0.0461 as R2 score and 0.3488 as MAPE. Then i plotted the model for evaluation and it turned out that it did not perform as expected.
    
14.  In CatBoost Regression i got 0.8527 as R2 score and 0.1647 as MAPE. Then i plotted the model for evaluation and it turned out that it performed way better than the previously trained models.
    
15.  I Hyper Tuned the CatBoost Regression model. i got 0.8189 as R2 score and 0.1863 as MAPE. Which is not as good as the regular CatBoost Regression model. Then we plotted the model for evaluation.
    
16.  I Hyper Tuned the XGBoost model. i got 0.8553 as R2 score and 0.1627 as MAPE. Which is better than the regular XGBoost Regression & CatBoost models. Then i plotted the model for evaluation.
    
17.  Finally, i Hyper Tuned the Linear Regression model. i got 0.6298 as R2 score and 0.3058 as MAPE. Then i plotted the model for evaluation.
    

### So, i came to a conclusion that the Hyper Tuned XGBOOST Regression model is the ideal machine learning model for house price prediction in this dataset. 


