# Medical Insurance Cost Prediction

This repository contains a single Jupyter notebook, **`Medical Insurance.ipynb`**, that explores and models medical insurance charges using classical machine learning.

> **Notebook last processed:** 2025-10-10 17:00 (local build time for this README)

---

## 📌 Project Objective
- Perform **exploratory data analysis (EDA)** on a medical insurance dataset.
- **Encode categorical features** and prepare data for modeling.
- Train a **Linear Regression** model to predict the **`charges`** column.
- Evaluate performance using **R² (coefficient of determination)**.
- Build a tiny **predictive system** that estimates cost for a sample input.

---

## 🧾 Dataset & Features
The notebook expects a CSV named **`insurance.csv`** (Colab path in the notebook is `/content/insurance.csv`).  
Core columns used in the workflow:

- **Numerical:** `age`, `bmi`, `children`, `charges` *(target)*  
- **Categorical:** `sex`, `smoker`, `region`

### Categorical Encodings (as in the notebook)
- `sex`: `male → 0`, `female → 1`  
- `smoker`: `yes → 0`, `no → 1`  
- `region`: `southeast → 0`, `southwest → 1`, `northeast → 2`, `northwest → 3`

> ⚠️ Note: The `smoker` mapping sets **yes=0** and **no=1** (this is directly from the notebook).

---

## 🔎 Exploratory Data Analysis (EDA)
The notebook includes basic visualizations with **Matplotlib** and **Seaborn**, such as:
- Distributions: `age`, `bmi`, `charges`
- Counts: `sex`, `smoker`, `region`

These plots help understand the spread of numerical features and the balance of categorical variables.

---

## 🧰 Tech Stack
- **Python**, **NumPy**, **Pandas**
- **Matplotlib**, **Seaborn**
- **scikit-learn**: `train_test_split`, `LinearRegression`, `metrics`

---

## 🧪 Modeling Workflow
1. **Load data** from `insurance.csv`.
2. **EDA** with distribution and count plots.
3. **Encode categoricals** using `DataFrame.replace` (see mappings above).
4. **Feature/Target split**
   ```python
   X = insurance_dataset.drop(columns='charges', axis=1)
   Y = insurance_dataset['charges']


So, I have got the training data accuracy as 75%
and the test data accuracy as 74%, I feel like the model performancy can be imporved in future

--If you like my project please leave a "STAR". Thank you
