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

This dataset can be used for a variety of tasks, such as regression analysis, data exploration and visualization, feature engineering, and more. So, we build models that predict housing prices based on various features and can provide insights into the relationships between housing prices and various demographic factors.

## Methodology

1.  At first we imported all the necessary libraries into our project.
    
2.  Then we load the dataset.
    
3.  Afterwards, we checked the columns and their data types.
    
4.  We found the ocean_proximity column as an object.
    
5.  Then we checked for null values in our dataset. There are 207 null values in the bedrooms column.
    
6.  We replaced the null bedroom values with room values. Now there are no null values left in the dataframe.
    
7.  Then we encoded the ocean proximity column.
    
8.  Afterwards we checked the correlation heatmap for our dataframe.
    
9.  We checked the median house value column distribution of our dataframe.
    
10.  Then splitted our data into train and test respectively 80/20 splits.
    
11.  Then we trained Linear Regression, XGBoost and Catboost for our dataframe.
    
12.  In linear regression we got 0.6298 as R2 score and 0.3058 as MAPE (Mean Absolute Percentage Error). Then we plotted the model for evaluation .
    
13.  In XGBoost we got -0.0461 as R2 score and 0.3488 as MAPE. Then we plotted the model for evaluation and it turned out that it did not perform as expected.
    
14.  In CatBoost Regression we got 0.8527 as R2 score and 0.1647 as MAPE. Then we plotted the model for evaluation and it turned out that it performed way better than the previously trained models.
    
15.  Then we Hyper Tuned the CatBoost Regression model. We got 0.8189 as R2 score and 0.1863 as MAPE. Which is not as good as the regular CatBoost Regression model. Then we plotted the model for evaluation.
    
16.  Afterwards we Hyper Tuned the XGBoost model. We got 0.8553 as R2 score and 0.1627 as MAPE. Which is better than the regular XGBoost Regression & CatBoost models. Then we plotted the model for evaluation.
    
17.  Finally, we Hyper Tuned the Linear Regression model. We got 0.6298 as R2 score and 0.3058 as MAPE. Then we plotted the model for evaluation.
    

### So, we came to a conclusion that the Hyper Tuned XGBOOST Regression model is the ideal machine learning model for house price prediction in this dataset. 

## Conclusion

This California Housing Prices Dataset is a great resource for those looking to dive into regression analysis, explore and visualize housing prices in California, or use various demographic factors to predict housing prices. With its well-curated data, this dataset can be a valuable asset to any data scientist's toolkit.
