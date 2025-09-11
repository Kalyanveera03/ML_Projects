# 🩺 Diabetes Prediction Project

This project predicts whether a person is diabetic or not based on health-related diagnostic measurements such as glucose level, BMI, age, etc.  
It uses machine learning techniques to preprocess data, train a classifier, evaluate accuracy, and make predictions for new input data.

---

## 📊 Dataset

We use the **Pima Indians Diabetes Dataset**, which contains the following features:

| Feature | Description |
|--------|-------------|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skinfold thickness (mm) |
| Insulin | 2-Hour serum insulin (mu U/ml) |
| BMI | Body mass index (weight/height²) |
| DiabetesPedigreeFunction | Diabetes pedigree function (genetic risk) |
| Age | Age (years) |
| Outcome | `0` = Not Diabetic, `1` = Diabetic |

---

## 🧠 Project Workflow

1. **Data Loading & Exploration**
   - Loaded dataset using Pandas.
   - Checked for missing values and performed basic EDA.

2. **Data Preprocessing**
   - Split dataset into training and test sets.
   - Scaled features using `StandardScaler` to normalize data.

3. **Model Training**
   - Trained a machine learning classifier (e.g., Logistic Regression, SVM, or other).
   - Tuned parameters for better performance.

4. **Evaluation**
   - Computed **accuracy score** on both training and test sets.
   - Printed results to evaluate model generalization.

5. **Prediction on New Data**
   - Accepted user input (single row).
   - Scaled input using the trained `StandardScaler`.
   - Predicted diabetes status and printed result.

---

## 🛠 Fix Summary

During review of the notebook, the following issues were identified and fixed:

### 1️⃣ StandardScaler Warning Fix

**Issue:**  
You were calling `scaler.transform(input_data_reshaped)` where `input_data_reshaped` was a NumPy array.  
Since `scaler` was fit on a DataFrame with column names (`X_train`), scikit-learn issued a warning:

> `UserWarning: X does not have valid feature names, but StandardScaler was fitted with feature names`

**Fix:**  
Wrapped the input into a DataFrame with the same columns as `X_train`:

```python
std_data = scaler.transform(pd.DataFrame(input_data_reshaped, columns=X_train.columns))
