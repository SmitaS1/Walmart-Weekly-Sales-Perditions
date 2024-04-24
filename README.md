<p align="center">
  <img src="dataset-cover.jpeg" width="600">
</p>

## Project Objective

### Introduction

Walmart, as one of the premier multinational retail giants, operates in a highly competitive retail landscape. To maintain its market leadership, Walmart relies on strategic decisions driven by insightful data analysis.

### Objective

This project aims to leverage past data from Walmart stores through rigorous exploratory data analysis (EDA) to construct a predictive model capable of accurately forecasting Weekly Sales. Such a model serves as a powerful tool for business managers, empowering them to uncover critical insights and identify areas for enhanced strategic planning.

### Key Contributions

- **Strategic Decision Support**: Our predictive model provides actionable insights to Walmart's leadership, enabling them to make informed decisions crucial for maintaining market dominance.
- **Identifying Business Weaknesses**: By scrutinizing past data, our model identifies potential shortcomings in business planning, enabling proactive measures to address them effectively.
- **Enhanced Planning Efficiency**: With the ability to anticipate Weekly Sales, Walmart can optimize resource allocation, streamline operations, and bolster overall efficiency.

### Conclusion

In the fiercely competitive retail sector, the ability to forecast Weekly Sales accurately is indispensable for Walmart's sustained success. Our predictive model, born out of comprehensive exploratory data analysis, stands as a testament to Walmart's commitment to innovation and strategic foresight.

## Table of Contents

<details open>
<summary>Show/Hide</summary>
<br>

### Data Source

- **Source**: The dataset is sourced from Kaggle.
- **URL**: [Walmart Sales Prediction Dataset](https://www.kaggle.com/code/yasserh/walmart-sales-prediction-best-ml-algorithms/input)

### Data Analysis

- **Columns**:
  - Store: Store number (1-45)
  - Date: Week of sales (2010, 2011, 2012)
  - Weekly_Sales: Sales for the given store
  - Holiday_Flag: Whether the week is a special holiday week (1 – Holiday week and 0 – Non-holiday week)
  - Temperature: Temperature on the day of sale
  - Fuel_Price: Cost of fuel in the region
  - CPI: Prevailing consumer price index
  - Unemployment: Prevailing unemployment rate

1. [File Descriptions](#File_Description)
2. [Technologies Used](#Technologies_Used)
3. [Structure](#Structure)
4. [Summary](#Summary)
   * [Data Cleaning](#Data_Cleaning)
   * [Data Analysis](#Data_Analysis)
   * [Modelling, Hyperparameter Tuning & Evaluation](#Modelling)
       * [Conclusion](#Conclusion)
       * [Future Improvements](#Future_Improvements)
</details>

## File Descriptions

<details>
<a name="File_Description"></a>
<summary>Show/Hide</summary>
<br>

- **Final_project**: Folder containing all data files
    - **Walmart.csv**: Data before any changes
    - **df_date_convert.csv**: Data after checking for null and duplicate values and converting 'Date' column to datetime, extracting year, month, day, and week from Date
    - **df2_data.csv**: Save DataFrame to a CSV file for Neural Networking Model
    - **X_linear_data.csv**: Splitting data and saving the X data in CSV file
    - **y_linear_data.csv**: Splitting data and saving the y data in CSV file
    - **df_split_date_data.csv**: Fluctuation to split year into four seasons then correct data format of the 'date' column
    - **df_data_after_drop.csv**: Save DataFrame to a CSV file after dropping unwanted columns
    - **df_drop_outlier.csv**: Save DataFrame to a CSV after dropping outliers
</details>

## Technologies Used

<details>
<a name="Technologies_Used"></a>
<summary>Show/Hide</summary>
<br>
    
- Python
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scikit-Learn
- Sklearn
- Plotly
- Tensorflow
- Category_encoders
</details>

## Structure

<details>
<a name="Structure"></a>
<summary>Show/Hide</summary>
<br>

  * 1.1 Import 
  * 1.2 Data Understanding
  * 1.3 Checking for Nulls
  * 1.4 Check Duplicated Data
  * 1.5 Feature Engineering: Date Variable
  * 1.6 Data Distribution
    * 1.6.1 Data Distribution: Target
    * 1.6.2 Data Distribution: Numerical Features
    * 1.6.3 Data Distribution: Categorical Features
  * 1.7 Feature Analysis
    * 1.7.1 Feature Analysis: Holiday_Flag vs Weekly_Sales
    * 1.7.2 Feature Analysis: Month, Year vs Weekly_Sales
    * 1.7.3 Feature Analysis: Histogram to show the distribution of the data for Unemployment, Fuel Price, Temperature, and Weekly_Sales
  * 1.8 Finding and Handling Outliers
  
</details>
   
## Summary

<a name="Data_Cleaning"></a>
### Data Cleaning

<details open>
<summary>Show/Hide</summary>
<br>

Walmart dataset consists of 6435 rows and 8 columns, with the target column being Weekly_Sales. The dataset is quite clean, with no missing values and duplicate values. A total of 497 rows of outlier data were identified and dropped.
</details>

<a name="Data_Analysis"></a>
### Data Analysis

<details open>
<summary>Show/Hide</summary>
<br>

From the Annual Sales graph, it can be seen that the largest sales occurred in 2011, followed by 2010 and 2012. It should be noted that the data ranges are not balanced every year.
</details>


<a name="Modelling, Hyperparameter Tuning & Evaluation"></a>
## Modelling

<details open>
<summary>Show/Hide</summary>
<br>

### Neural Networking/ Deep Learning Model

- Split training/test datasets
- Preprocess numerical data for neural network
- Create a StandardScaler instances
- Fit the StandardScaler and finally Scale the data

### Logistic Regression Model

- Import from SKLearn
- Assign random_state parameter
- Fit the model using training data
- Make a prediction using the testing data
- Generate Confusion Matrix
- Print Classification Report

### Linear Regression

- Split data for train and test
- Split data into Numerical and Categorical features
- Create data transformation pipeline
- Fit the training data
- Transform the training and testing data
- Fit the data to the Linear Regression Model
- Create a function to distribute our plot
- Plot the predicted values using training data compared to the actual values of the training data

### Define Polynomial Regression Model 

- Model Evaluation: Define a function to evaluate the model performance, typically using metrics like Mean Squared Error (MSE), R-squared.
- Predict Data: Use the model to predict outputs using both the training and testing data.
- Parameter Tuning: Tune the hyperparameters of the polynomial regression model. This can involve techniques like grid search or randomized search to find the

## Conclusion

The best model for predicting weekly sales is Polynomial Regression. This model can provide information that helps business managers identify and understand weaknesses in business planning. The Marketing Division should increase advertising during the weeks after Christmas and before Thanksgiving. Additional personnel from the Logistics division may be needed in November-December because sales increased significantly compared to other months. It's also advisable to ensure sufficient restocking of goods on weekdays to minimize production costs.

## Future Improvements

Potential future improvements for this project include:

- Trying a different pre-processing approach to see if model performances change.
- Bringing in new sources of data to analyze if there are significant differences in the predictive power based on additional factors.