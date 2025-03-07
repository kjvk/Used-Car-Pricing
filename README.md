# Used Car Price Prediction Project

## Business Understanding
From a business perspective, the task is to identify the key factors that influence the prices of used cars. This can be reframed as a data problem by stating that we aim to build a predictive model that can accurately estimate the prices of used cars based on various features such as mileage, age, brand, model, fuel type, and so on. The technical vocabulary includes terms like regression analysis, feature engineering, and model evaluation.

## Data Understanding
To get familiar with the dataset and identify any quality issues, we would take the following steps:
- Load the dataset into a pandas DataFrame.
- Check the first few rows of the dataset using `head()` to understand its structure.
- Check the data types of each column to ensure they are appropriate.
- Check for missing values and decide how to handle them (imputation or removal).
- Explore summary statistics of numerical columns to understand their distributions.
- Plot histograms or boxplots for numerical variables to identify outliers.
- Explore unique values of categorical variables and their frequency distributions.
- Visualize relationships between features and the target variable using scatter plots or boxplots.
![](images/PA11_Data.png)
![](images/PA11_Null_Data.png)
![](images/PA11_cars_1995.png)

## Data Preparation
After understanding the data, we need to prepare it for modeling. This involves:
- Handling missing values by imputation or removal.
- Encoding categorical variables using techniques like one-hot encoding, TargetEncoding.
- Scaling numerical features to a similar range using StandardScaler,MinMAxScaler,RobustScaler
- Feature engineering
- Splitting the dataset into training and testing sets.
![](images/PA11_Drive_Types.png)
![](images/PA11_Car_Colors.png)
![](images/PA11_year_vs_Price.png)
![](images/PA11_corr.png)
![](images/PA11_Robust_Scaler.png)
- After EDA
![](images/PA11_after_EDA.png)
## Modeling
Now, we'll build regression models using the prepared dataset:
- Define a pipeline for preprocessing (encoding, scaling) and modeling (e.g., Linear, Ridge, Lasso Regressors or XGBRegressor).
- Use GridSearchCV to search for the best hyperparameters of the models.
- Train the models using the training dataset.
- Evaluate the models using cross-validation to assess their performance.
- Compare the performance of different models and select the best-performing one.
![](images/PA11_LR_DF.png)
![](images/PA_11_LR_coef.png)
![](images/PA11_RD_DF.png)
![](images/PA_11_RD_coef.png)
![](images/PA11_LO_DF.png)
![](images/PA_11_LO_coef.png)
![](images/PA11_XG_DF.png)
![](images/PA_11_XG_coef.png)
## Evaluation
After building and evaluating the models, we need to reflect on whether they meet the business objective of identifying key drivers of used car prices:
- Assess the performance metrics (e.g., RMSE, R-squared) of the models.
- Interpret the coefficients or feature importances to identify the most influential factors.
- Determine if the models provide meaningful insights into the pricing factors.
- Decide if any adjustments are needed in earlier phases (data understanding, preparation) based on the findings.
- Summarize the findings and prepare to communicate them to the client.
- When compared the results of Linear Vs XGBoost Regressors,XGB has performed better and provided the importanti features to consider while buying the used cars.
## Deployment
Finalize the XGBoost model and convert it to pickle file for prediction and inference.

###### Ref https://github.com/mo-adi
