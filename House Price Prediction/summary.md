# 🏡 House Price Prediction Project

This project predicts **house prices** based on various features such as crime rate, number of rooms, property tax rate, etc.  
It uses **machine learning techniques** to preprocess data, train a regression model, evaluate its accuracy, and make predictions on new input data.

---

## 📊 Dataset

We use the **Boston Housing Dataset**, which contains the following features:

| Feature | Description |
|--------|-------------|
| CRIM | Per capita crime rate by town |
| ZN | Proportion of residential land zoned for lots over 25,000 sq.ft. |
| INDUS | Proportion of non-retail business acres per town |
| CHAS | Charles River dummy variable (1 if tract bounds river, 0 otherwise) |
| NOX | Nitric oxide concentration (parts per 10 million) |
| RM | Average number of rooms per dwelling |
| AGE | Proportion of owner-occupied units built prior to 1940 |
| DIS | Weighted distances to five Boston employment centres |
| RAD | Index of accessibility to radial highways |
| TAX | Full-value property tax rate per $10,000 |
| PTRATIO | Pupil-teacher ratio by town |
| B | 1000(Bk - 0.63)² where Bk is the proportion of Black residents |
| LSTAT | Percentage of lower status of the population |
| PRICE | Median value of owner-occupied homes (target) |

---

## 🧠 Project Workflow

1. **Data Loading & Exploration**
   - Loaded dataset using Pandas.
   - Renamed `MEDV` to `price` for clarity.
   - Checked for missing values and reviewed summary statistics.

2. **Exploratory Data Analysis**
   - Plotted a **correlation heatmap** using Seaborn.
   - Identified features most correlated with house price (positive & negative).

3. **Data Splitting**
   - Split dataset into **training** and **test** sets (80/20 split).

4. **Model Training**
   - Trained a regression model using **XGBRegressor**.
   - Learned relationships between features and target price.

5. **Evaluation**
   - Computed **R² score** on both training and test data.
   - Measured **Mean Absolute Error (MAE)** to check prediction error.

6. **Prediction on New Data**
   - Accepted user input (new house features).
   - Predicted house price using the trained model.

---

## 📈 Model Performance

| Metric | Training | Test |
|-------|----------|------|
| **R² Score** | ~0.999 (excellent fit) | ~0.87 (good generalization) |
| **MAE** | Very low (close to 0) | Low |

✅ The model performs very well and generalizes nicely on unseen data.

---



