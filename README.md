
# Predictive Analysis of Used Car Prices

## Introduction

This project focuses on predicting used car prices by applying data analysis and machine learning techniques. It includes data preparation, feature engineering, EDA and model building to estimate car prices accurately using regression models.



## Dataset Introduction

The dataset used in this project is an open dataset from 1985 on used car prices, originally compiled by Jeffrey C. Schlimmer. It contains 26 attributes related to various car features, such as insurance risk level (symboling), average loss payment (normalized losses), make, fuel type, and more. Each attribute provides detailed information about different aspects of the cars, helping to capture the diverse factors that influence their characteristics.


## Dependencies

Python 3.x, pandas, numpy, scikit-learn, matplotlib, seaborn, Statsmodels

## Data Cleaning and Preprocessing

![Screenshot 2024-08-13 174320](https://github.com/user-attachments/assets/ce7183f8-6a7a-4f40-b42d-8c4d55b6e341)

### Handling Missing Values:

To prepare the dataset for analysis, I addressed missing values as follows:

- Replaced placeholders: Missing values represented by "?" were replaced with NaN to facilitate easier processing.
- Dropped incomplete rows: Rows with missing values in the target variable were removed to maintain the integrity of the predictive analysis.
- Imputed numeric data: Missing values in numeric columns were filled with the mean of their respective columns to avoid introducing bias.
- Imputed categorical data: Missing values in categorical columns were replaced with the most frequent value to reflect the most common scenario.

### Data Formatting:

- Data type conversion: Converted certain columns to appropriate data types (e.g., converting numerical data stored as strings to float or integer) to ensure consistent and accurate analysis.

![Screenshot 2024-08-13 174628](https://github.com/user-attachments/assets/44abb068-8642-4558-b42e-1926db03d55a)

## Feature Engineering

### Normalization: 
- Scaled numeric features to a common range (e.g., between 0 and 1) to ensure that no single feature dominated the analysis due to its scale.
  
![Screenshot 2024-08-13 174801](https://github.com/user-attachments/assets/495037d6-aec3-4af1-ab38-657a53bfe439)

### Binning: 
- Categorized continuous variables into discrete bins to simplify the analysis and improve interpretability.

![Screenshot 2024-08-13 175052](https://github.com/user-attachments/assets/c21835b0-6c0b-4945-b69c-94d77d98ff3a)

### One-Hot Encoding: 
- Converted categorical variables into binary (0/1) variables to enable their use in model building.

![Screenshot 2024-08-13 175216](https://github.com/user-attachments/assets/e3a94a96-641a-4f52-b7cd-e29641f3febb)

### Creating new variables: 
- Derived additional columns like fuel efficiency in L/100km from existing data to provide more relevant metrics for analysis.

## Exploratory Data Analysis for Feature Selection

### Correlation Analysis:
- Correlation: Examined the correlation between continuous variables and the target variable (price) to identify strong predictors.
- Scatter Plots: Used sns.regplot to visualize the relationship between independent variable and the dependent variable price.

![Screenshot 2024-08-13 175419](https://github.com/user-attachments/assets/c8dbfd67-2620-4c08-9b54-c7164012b6c2)

### Categorical Variable Analysis:
- Box Plots: Analyzed the relationship between categorical variables (body-style, engine-location, drive-wheels) and price using box plots to understand how different categories affect car prices.

![Screenshot 2024-08-13 175627](https://github.com/user-attachments/assets/2974546f-6da3-4cf5-93b7-969f352d6917)

### Group Statistics:

- Aggregated Analysis: Grouped data by drive-wheels and body-style to compute mean prices and observed patterns in how these factors influence the price.

![Screenshot 2024-08-13 175756](https://github.com/user-attachments/assets/2da260d6-72c5-4f81-b9e0-2dfe8c5acc20)

### Statistical Significance Testing:

- Pearson Correlation Coefficient: Calculated the Pearson correlation coefficient and p-values to assess the strength and significance of the relationship between various features and the target variable.

![Screenshot 2024-08-13 175917](https://github.com/user-attachments/assets/138671f4-50f3-4200-9587-1726f5c57bb5)

## Model Building 

### Linear Regression Model
- Model Training: Built a linear regression model using scikit-learn and trained it on the prepared dataset.
- Model Evaluation: Evaluated the model's performance by calculating the R-squared value and mean squared error (MSE). The R-squared value was approximately 0.817, indicating a good fit, while the MSE provided insight into the prediction accuracy.

![Screenshot 2024-08-13 180111](https://github.com/user-attachments/assets/55201471-7c50-4a9b-9d5b-12780a06770d)

![Screenshot 2024-08-13 180250](https://github.com/user-attachments/assets/d84100de-7f34-4897-aa26-6ea46036192c)

![Screenshot 2024-08-13 180404](https://github.com/user-attachments/assets/83dbad72-791f-4ea5-b991-01fb238cffda)

### Polynomial Regression Model
- Feature Transformation: Applied polynomial feature transformation to capture non-linear relationships between features and the target variable.
- Model Training: Trained a polynomial regression model of degree 2 on the transformed features.
- Model Evaluation: Assessed the polynomial regression model’s performance, which yielded a higher R-squared value of approximately 0.881, indicating an improved fit compared to the linear model. The MSE for this model was lower, reflecting better prediction accuracy.

![Screenshot 2024-08-13 180536](https://github.com/user-attachments/assets/55e69a76-3180-4d7a-bf18-94c0d53ec541)

![Screenshot 2024-08-13 180723](https://github.com/user-attachments/assets/1433fbfa-64f8-44af-a617-416be1b6a339)

## Conclusion

In this project, I conducted a comprehensive predictive analysis of used car prices using a dataset from 1985. Through data cleaning and preprocessing, including handling missing values and normalizing features, I ensured that the dataset was well-prepared for analysis. Feature engineering techniques such as normalization, binning, and one-hot encoding were applied to enhance the dataset's suitability for modeling. Exploratory Data Analysis (EDA) provided valuable insights into the relationships between various features and car prices, identifying key predictors. 

I built and evaluated both linear and polynomial regression models, finding that the polynomial regression model outperformed the linear model in terms of fit and prediction accuracy.

## Future Work

- Hyperparameter Tuning: Further optimize the models by experimenting with different parameters.
- Model Expansion: Explore other advanced models like Ridge Regression.






