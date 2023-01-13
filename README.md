# Beau Home House Prices Prediction Using Machine Learning
Strategy & Analytics Consultant: Dima Taher 

# GitHub Navigation Instructions 

- For a detailed overview of the complete project, please reference this [notebook.](House Price Predictions Using ML.ipynb)
- For the Dataset used, it will be found [here.](Data/house_data_set.csv)


# Overview
In effort to build a house price prediction model, three machine learning models were built, evaluated, and compared to each other to determine which model provided the most accurate results. The results lead to the following recommendation for Beau Home Properties:

    - Beau Home Properties is recommended to use the Random Forest Model since it provided the most accurate results.
    
The full presentation for this project can be found here.


# Business Understanding

## The Problem
Beau Home Properties is a new Real Estate Company that is just starting out in the State of California. They will be entering the business of investing in properties by buying and selling. They reached out to our Data Science team to build a value estimation system that can automatically deduce the value of the houses. 


## The Goal
This project will focus on building a machine learning model trained on existing housing features to predict house prices.
The goal is to identify the key features that influence house prices and after that will focus on building a machine learning model trained on those housing features to predict house prices. Three models will be built: Linear Regression, Random Forest, and XGBoost.


# Data Understanding and Analysis

## Data Sources, Descriptions, Relevant Visualizations
The dataset used is from [LiknedIn Learning.](https://www.linkedin.com/learning/machine-learning-and-ai-foundations-value-estimations/explore-a-home-value-data-set?autoplay=true&resume=false&u=1504) It contained information on houses in different cities in California, it originally included 20 columns and 42703 rows. This project used 15 total features from this dataset. 

The 15 feautures are: 
    year_built             
    stories                
    num_bedrooms           
    full_bathrooms         
    half_bathrooms         
    livable_sqft          
    total_sqft             
    garage_type            
    garage_sqft            
    carport_sqft           
    has_fireplace          
    has_pool               
    has_central_heating    
    has_central_cooling    
    city


# Methods

## Programming Methods
Language: Python 3.8.5 

Major Packages and Version Numbers can be found [here.](requirements.txt)


# Data Preparation and Machine Learning Models

The data was cleaned and explored in detail before drawing any conclusions. That helps inspecting the data better and getting a more accurate general understanding of the data at hand.
Some features were not useful and didn't need to be included in the ML models, therefore, these columns were dropped: house_number, street_name, unit_number, zip_code.

The data was checked for duplicate and null values and none were available. 

After preparing the data, the numerical features were prepared into dicrete and continuous variable. These features were later on visualized in relation to the house prices which is our target variable.

The data contained only two categorical variables: garage_type and city. One-Hot Encoding was used on these variables which means creating dummy variables to turn it into numerical values so that it can be used in the models.


## Modeling

For this section, the data was split into train and test sets, 70% for the training set and 30% for the testing set which will be used in the models.

The first model is Linear Regression, this model will be used as a baseline model. The second is a random forest, and the third is created using XGBoost. The three models will then be compared together.

For the evaluation of the models' performances, three metrics are being focused on which are the R-Squarred (R^2), Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE). 

## Results

The results for each model were as follows: ![My Image](model results.jpg)

Random Forest performed best in all metrics, the model is explaining about 77% of the variance in house sale prices vs. 75% for XGBoost and 63% for linear regression. The MAE value is telling us that the model is off by about 59,265 USD in a given prediction vs. 62,197 USD for XGBoost and 94,602 USD for Linear Regression. 

When we put all the models together and compare we can see that the Random Forest Model has the best accuracy results in all the metrics.



# Business Recommendation:

Based on the outlined analyses above, it is recommended for Beau Home Properties to use the random forest model for their house price predictions. This model will provide Beau Home Properties with accurate results and will make the process of valuating house prices more efficient.



