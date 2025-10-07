# ❤️ Heart Disease Prediction Project
This project predicts **heart disease** in patients based on various medical features such as age, blood pressure, cholesterol levels, chest pain type, etc.  
It uses **machine learning techniques** to preprocess data, train a classification model, evaluate its accuracy, and make predictions on new patient data.

---

## 📊 Dataset
We use a **Heart Disease Dataset** containing medical records of 303 patients with the following features:

| Feature | Description |
|--------|-------------|
| age | Age of the patient |
| sex | Gender (1 = male, 0 = female) |
| cp | Chest pain type (0-3) |
| trestbps | Resting blood pressure (mm Hg) |
| chol | Serum cholesterol (mg/dl) |
| fbs | Fasting blood sugar > 120 mg/dl (1 = true, 0 = false) |
| restecg | Resting electrocardiographic results (0-2) |
| thalach | Maximum heart rate achieved |
| exang | Exercise-induced angina (1 = yes, 0 = no) |
| oldpeak | ST depression induced by exercise relative to rest |
| slope | Slope of the peak exercise ST segment (0-2) |
| ca | Number of major vessels colored by fluoroscopy (0-4) |
| thal | Thalassemia (0-3) |
| target | Heart disease diagnosis (1 = disease, 0 = healthy) |

**Class Distribution:**
- Heart Disease Present: 165 patients (54.5%)
- Healthy: 138 patients (45.5%)

---

## 🧠 Project Workflow

1. **Data Loading & Exploration**
   - Loaded dataset using Pandas.
   - Checked dataset shape: 303 rows × 14 columns.
   - Verified no missing values in the dataset.
   - Reviewed summary statistics using `describe()`.

2. **Exploratory Data Analysis**
   - Analyzed data distribution and statistics.
   - Examined target variable distribution.
   - Verified data types and checked for null values.

3. **Data Splitting**
   - Split dataset into **training** and **test** sets (80/20 split).
   - Used stratified split to maintain class distribution.
   - Training samples: 242
   - Test samples: 61

4. **Model Training**
   - Trained a classification model using **Logistic Regression**.
   - Learned relationships between medical features and heart disease diagnosis.

5. **Evaluation**
   - Computed **Accuracy Score** on training data.
   - Model demonstrates good predictive capability.

6. **Prediction on New Data**
   - Accepted user input (new patient's medical features).
   - Predicted heart disease presence using the trained model.

---

## 📈 Model Performance

| Metric | Training |
|-------|----------|
| **Accuracy Score** | **85.12%** (good fit) |

✅ The model performs well and can effectively classify patients with and without heart disease.

---

## 💻 How to Use

### Installation
```bash
pip install numpy pandas scikit-learn
```

### Running the Model
```python
# Example patient data
input_data = (62, 0, 0, 140, 268, 0, 0, 160, 0, 3.6, 0, 2, 2)

# Reshape for prediction
input_data_as_numpy_array = np.asarray(input_data)
input_data_reshaped = input_data_as_numpy_array.reshape(1, -1)

# Make prediction
prediction = model.predict(input_data_reshaped)

if prediction[0] == 0:
    print('The Person does not have Heart Disease')
else:
    print('The Person has Heart Disease')
```

---

## 🛠️ Technologies Used
- **Python 3.x**
- **NumPy** - Numerical computations
- **Pandas** - Data manipulation and analysis
- **Scikit-learn** - Machine learning implementation
  - Logistic Regression
  - Train-test split
  - Accuracy metrics

---

## 📁 Repository Structure
```
├── Heart_Disease_Prediction.ipynb    # Main Jupyter notebook
├── data.csv                          # Dataset
└── README.md                         # Project documentation
```

---

## 🔮 Future Enhancements
- Evaluate model on test data
- Implement cross-validation for robust evaluation
- Try other algorithms (Random Forest, SVM, Neural Networks)
- Add confusion matrix and ROC curve analysis
- Perform hyperparameter tuning
- Create feature importance analysis
- Develop web application for real-time predictions

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.



---

⭐ **If you found this project helpful, please give it a star!**
