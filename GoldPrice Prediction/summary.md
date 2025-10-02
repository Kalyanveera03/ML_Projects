# Gold Price Prediction Project

## Introduction
This project focuses on predicting the price of gold (GLD) using historical financial data. The dataset consists of **2290 records** with features including stock market index (SPX), crude oil (USO), silver (SLV), and currency exchange rates (EUR/USD). The target variable is the price of gold (GLD).

## Data Collection & Processing
- Dataset: `gld_price_data.csv`
- Shape: 2290 rows × 6 columns
- Columns:
  - Date
  - SPX (S&P 500 index)
  - GLD (Gold ETF price – target)
  - USO (Crude Oil ETF price)
  - SLV (Silver ETF price)
  - EUR/USD (Currency exchange rate)

### Steps Performed
1. Imported libraries (`numpy`, `pandas`, `matplotlib`, `seaborn`, `sklearn`).
2. Loaded and inspected the dataset.
3. Checked for missing values – none found.
4. Converted and processed the data for analysis.

## Exploratory Data Analysis (EDA)
- Correlation analysis performed to understand relationships:
  - Positive correlation: GLD vs SLV, EUR/USD.
  - Negative correlation: GLD vs USO, SPX.
- Visualizations (heatmaps, line plots, pair plots) were used to study feature relationships.

## Feature Engineering
- Selected independent variables: SPX, USO, SLV, EUR/USD.
- Target variable: GLD (Gold Price).

## Model Development
- Dataset split into training and testing sets.
- Regression models applied:
  - Linear Regression
  - Random Forest Regressor (main model used)
- Model evaluation done using R² Score and Mean Absolute Error (MAE).

## Results
- Random Forest Regressor outperformed Linear Regression.
- Achieved **high accuracy** in predicting gold prices.
- Visual comparison between actual vs predicted prices confirmed strong performance.

## Conclusion
- Gold price prediction can be effectively modeled using historical financial indicators.
- Random Forest proved to be the best-performing algorithm in this project.
- This model can be extended to real-world financial forecasting with further optimization.

---
**Author:** Sai Kalyan Veera  
**Tools Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
