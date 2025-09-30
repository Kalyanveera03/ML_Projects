# Wine Quality Prediction Project

## Introduction
This project focuses on predicting the quality of wine based on its physicochemical features using machine learning techniques. The dataset used is the **Wine Quality Red Dataset** (`winequality-red.csv`).

## Data Collection
The dataset was loaded using **Pandas** from the CSV file. It contains multiple physicochemical features (e.g., acidity, chlorides, alcohol) and a target variable `quality` ranging from 0–10.

## Data Analysis and Visualization
- Conducted **exploratory data analysis (EDA)** with Pandas, Matplotlib, and Seaborn.
- Checked dataset shape, missing values, and distributions.
- Visualized correlations between features and target using heatmaps and pairplots.
- Observed:
  - **Positive correlation**: Alcohol with quality  
  - **Negative correlation**: Volatile acidity with quality  

## Data Preprocessing
- Split dataset into **features (X)** and **target (y)**.
- Applied an 80/20 **train-test split**.
- Features were already numerical; no categorical encoding was needed.

## Model Building
- Implemented a **Random Forest Classifier** using scikit-learn.
- Trained the model on the training set.
- Predictions were made on both training and test data.

## Model Evaluation
- Evaluated model performance using **accuracy score**.
- The model achieved strong accuracy on the dataset, showing the effectiveness of Random Forest for classification.

## Conclusion
This project successfully demonstrated a complete machine learning workflow:
1. Data collection  
2. EDA and visualization  
3. Preprocessing  
4. Model building (Random Forest)  
5. Evaluation  

The Random Forest Classifier proved effective for predicting wine quality, with **alcohol content** and **volatile acidity** being key influencing factors.
