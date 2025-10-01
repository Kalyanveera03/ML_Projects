# Car Price Prediction Project

## Overview
This project predicts the **selling price of used cars** based on various features such as year, kilometers driven, fuel type, seller type, transmission, and ownership history.

## Dataset
- **Source:** CarDekho dataset  
- **Rows:** 4340  
- **Columns:** 8 (`name`, `year`, `selling_price`, `km_driven`, `fuel`, `seller_type`, `transmission`, `owner`)

## Data Preprocessing
1. Loaded dataset using **pandas**.  
2. Checked for null values (none found).  
3. Converted categorical variables into numerical values using **manual encoding**:
   - `fuel`: Petrol=0, Diesel=1, CNG=2, LPG=3, Electric=4  
   - `seller_type`: Dealer=0, Individual=1, Trustmark Dealer=2  
   - `transmission`: Manual=0, Automatic=1  
   - `owner`: First Owner=0, Second Owner=1, Third Owner=2, Fourth & Above Owner=3, Test Drive Car=4  

## Features & Target
- **Features (X):** `year`, `km_driven`, `fuel`, `seller_type`, `transmission`, `owner`  
- **Target (Y):** `selling_price`  

## Model Training
- Data split into **80% training** and **20% testing** using `train_test_split`.  
- Models used:
  - **Linear Regression**
  - **Lasso Regression (alpha=500)**  

## Model Evaluation
Metrics used:
- **R² Score**
- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**  

Results:
- Linear Regression achieved reasonable accuracy with R² ≈ 0.42 on training set.  
- Lasso Regression tested as a regularization approach.  

## Visualization
- Scatter plot of **Actual vs Predicted Prices** for Linear Regression.  

## Example Prediction
A car with:
- Year: 2015  
- KM Driven: 60000  
- Fuel: Petrol (0)  
- Seller Type: Individual (1)  
- Transmission: Manual (0)  
- Owner: First Owner (0)  

→ Model predicts the approximate **selling price**.  

## Conclusion
- The model successfully predicts car prices based on structured data.  
- Could be improved with more advanced algorithms (Random Forest, XGBoost, etc.) and feature engineering (e.g., extracting brand/model from `name`).  
