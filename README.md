## Objective
This project predicts the total number of bikes rented per hour using machine learning models.

## Model Used
Two regression models were trained and compared:
1. Linear Regression
2. LightGBM (Gradient Boosting Method)

The models were evaluated by evaluating RMSE(Root Mean Squared Error) and R2(Coefficient of Determination) metrics.

## Dataset
The dataset used is bike_sharing.csv, which contains the following features:
-Categorical features: season,year,month,hour,holiday,weekday,workingday,weather situation
-Numerical features: temperature,humidity,windspeed
-Target: count(cnt) - count of the total number of bikes rented

## Project Approach
1. Data preprocessing
- Drop the irrelevant columns: 'instant','dteday','casual','registered'
- Split the features into categorical and numerical types.
- Applied One-Hot Encoding to categorical features.
- Standardize numerical features using StandardScaler.

2. Model Training
- Split the data into 80% training sets and 20% testing sets.
- Trained both Linear Regression and LightGBM Regressor models using a pipeline that included the preprocessing steps.

3. Model Evaluation
- Calculated RMSE and R2 metrics on both training and test sets
- Selected the model with a higher R2 value and lower RMSE as the final model.

4. Visualization
- Created a scatter plot comparing actual vs predicted bike rental counts to visualize model performance

## Conclusion
The LightGBM model performed better than Linear Regression, achieving a lower RMSE and higher R2 value
Hence, LightGBM was selected as the final model for predicting hourly bike rentals.
