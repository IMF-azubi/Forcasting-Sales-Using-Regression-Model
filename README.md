# Time Series Regression Project
# Predictive-Modeling-for-Store-Sales
Explore accurate store sales forecasting with this time series analysis project. Leveraging Favorita's data, dive into predictive modeling, optimizing inventory, and gaining insights into sales patterns.

# Introduction
This project aims to analyze and predict sales data using time series regression techniques. The dataset consists of historical sales records with various features such as promotions, oil prices, and transaction details.

## Table of Contents
1. Project Overview
2. Data Exploration
    * Line Chart for 'onpromotion'
    * Resampling On Promotion Data
    * Sales Over Time
    * Oil Prices Over Time
    * Correlation Matrix
    * Sales Distribution Across Columns
    * Missing Values
3. Stationarity Testing (KPSS)
4. Answering Business Questions
    * Top 10 Stores by Sales
    * Top 5 Product Families
    * Dates with Lowest and Highest Sales Each Year
    * Impact of 2016 Earthquake on Sales
    * Correlation Between Promotions and Sales
5. Hypothesis Testing
    * Impact of Promotional Periods on Sales
6. Feature Processing/Engineering
7. Data Splitting
8. Models
    * Linear Regression
    * XGBoost Regression
    * CatBoost Regression
    * Gradient Boosting Regression
    * ARIMA
    * SARIMA
    * Decision Tree
9. Results
10. Summary and Insights
11. License
12. Acknowledgments
13. Author

# Project Overview
This project involves the analysis and prediction of sales data using various time series regression models. The dataset includes historical sales records with features such as promotions, oil prices, and transaction details. The goal is to gain insights into sales trends, answer specific business questions, and build predictive models for future sales.

# Data Exploration
*   Line Chart for 'onpromotion'
The line chart for the 'onpromotion' column indicates the presence or absence of promotional activities over time. Promotional activities were absent from January 2013 to March 2014, followed by a substantial increase observed over the subsequent years.

*   Resampling On Promotion Data
Resampling the 'onpromotion' data on both daily and monthly frequencies provides a clearer picture of promotional activities over time. The charts reveal distinct patterns and trends in promotional efforts.

*   Sales Over Time
The analysis of sales over time, with a focus on yearly seasonality, shows a positive increase across the years. Peaks at the end of each year suggest a yearly seasonality pattern in the sales data.

*   Oil Prices Over Time
The line chart for oil prices over time depicts the fluctuation in oil prices, providing insights into potential external factors that may influence sales.

*   Correlation Matrix
The correlation matrix explores the relationships between sales, onpromotion, transactions, and oil prices. A heatmap visualizes the strength and direction of these correlations.

*   Sales Distribution Across Columns
Box plots illustrate the distribution of sales across selected columns, including 'onpromotion,' 'is_holiday,' and 'stores_type.' These visualizations help identify potential patterns and variations.

*   Missing Values
Handling missing values involves methods such as 'bfill' for specific date-related columns, median imputation for skewed transaction data, and filling 'holiday_type' NaN values with 'No_holiday.'

# Stationarity Testing (KPSS)
Stationarity testing using the KPSS test is performed on sales data. The test helps determine whether the data is stationary or non-stationary.

# Answering Business Questions
1. Top 10 Stores by Sales
The analysis identifies the top 10 stores based on total sales. Visualizations provide insights into the sales performance of different stores.

2. Top 5 Product Families
Top 5 product families are determined based on total sales. A bar chart illustrates the total sales for each of these product families.

3. Dates with Lowest and Highest Sales Each Year
Dates with the lowest and highest sales for each year are identified and visualized using line plots. These visualizations provide insights into yearly sales patterns.

4. Impact of 2016 Earthquake on Sales
The impact of the 2016 earthquake on sales is assessed by analyzing sales trends around the earthquake period. Visualizations highlight any noticeable changes in sales during and after the earthquake.

5. Correlation Between Promotions and Sales
Scatter plots and correlation matrices explore the correlation between promotional activities and sales. The analysis reveals a moderate positive correlation, indicating a discernible relationship between promotions and sales.

# Hypothesis Testing
A t-test is conducted to determine the impact of promotional periods on store sales. The results indicate a statistically significant difference in sales between promotional and non-promotional periods.

# Feature Processing/Engineering
Additional features are extracted from the 'date' column, including month, day of the week, day of the month, and quarter. One-hot encoding is applied to categorical columns such as 'family,' 'city,' and 'state.' Numeric variables are scaled using Min-Max Scaling.

# Data Splitting
The dataset is split into training and evaluation sets based on the years, with data from 2013 to 2016 used for training and data from 2017 used for evaluation.

# Models
## XGBoost Regression
Model: XGBoost Regression
RMSLE: 0.23
RMSE: 0.63
MSE: 0.40
MAE: 0.27

## CatBoost Regression
Model: CatBoost Regression
RMSLE: 0.22
RMSE: 0.62
MSE: 0.39
MAE: 0.26

## Gradient Boosting Regression
Model: Gradient Boosting Regression
RMSLE: 0.24
RMSE: 0.68
MSE: 0.46
MAE: 0.31

## Decision Tree Regression
Model: Decision Tree Regression
RMSLE: 0.29
RMSE: 1.02
MSE: 1.05
MAE: 0.3

## Linear Regression
Model: Linear Regression
RMSLE: 0.26
RMSE: 0.94
MSE: 0.88
MAE: 0.43

## SARIMA
Model: SARIMA
RMSLE: 0.46
RMSE: 1.17
MSE: 1.37
MAE: 0.45

## ARIMA
Model: ARIMA
RMSLE: 0.47
RMSE: 1.23
MSE: 1.52
MAE: 0.53

# Results
| Model                        | RMSLE | RMSE | MSE  | MAE  |
| ---------------------------- | ----- | ---- | ---- | ---- |
| XGBoost Regression           | 0.23  | 0.63 | 0.40 | 0.27 |
| CatBoost Regression          | 0.22  | 0.62 | 0.39 | 0.26 |
| Gradient Boosting Regression | 0.24  | 0.68 | 0.46 | 0.31 |
| Decision Tree Regression     | 0.29  | 1.02 | 1.05 | 0.3  |
| Linear Regression            | 0.26  | 0.94 | 0.88 | 0.43 |
| SARIMA                       | 0.46  | 1.17 | 1.37 | 0.45 |
| ARIMA                        | 0.47  | 1.23 | 1.52 | 0.53 |

# Summary and Insights
The model "CatBoost Regression" demonstrate superior performance based on the RMSLE metric. This metric, known for assigning less significance to larger errors, enhances robustness against outliers. Given the considerable variation in sales across diverse regions, stores, and items in our scenario, the RMSLE metric emerges as a more suitable measure for evaluating model 
 
# Licence
This project is licensed under the MIT License. See the LICENSE file for details.

#  Acknowledgments
I would like to extend my appreciation to the https://www.azubiafrica.org/data-analytics for providing meaningful projects as an integral component of this program.

# Author
Isaac Mawuli Fumey