# 🏦 Loan Prediction using Machine Learning

## 📌 Project Overview
This project predicts whether a loan will be **approved or not** based on customer data. The solution uses **Support Vector Machine (SVM)** classification to model the relationship between applicant information (income, credit history, loan amount, etc.) and loan approval outcomes.

---

## 📂 Dataset
- **Source:** `dataloan.csv`  
- **Size:** ~600 rows  
- **Key Features:**
  - `Gender`, `Married`, `Education`, `Self_Employed`
  - `ApplicantIncome`, `CoapplicantIncome`, `LoanAmount`, `Loan_Amount_Term`
  - `Credit_History`
- **Target:** `Loan_Status` (1 = Approved, 0 = Rejected)

---

## 🛠️ Steps in the Notebook

### 1. **Data Collection & Processing**
- Imported necessary libraries: `numpy`, `pandas`, `seaborn`, `sklearn`
- Loaded dataset into a Pandas DataFrame
- Checked for missing values and handled them (if any)
- Converted categorical variables into numerical form using encoding

### 2. **Exploratory Data Analysis (EDA)**
- Visualized feature distributions using **Seaborn**
- Checked correlations between numerical variables
- Explored class balance (approved vs. rejected loans)

### 3. **Train-Test Split**
- Split data into training and testing sets  
- Used `train_test_split(..., stratify=Y, random_state=42)`  
  - ✅ `stratify` ensures balanced class distribution  
  - ✅ `random_state` ensures reproducible results  

### 4. **Model Training**
- Used **Support Vector Machine (SVC)** with linear kernel
- Trained model on the training data

### 5. **Model Evaluation**
- Predicted on test data
- Calculated **accuracy score** to measure performance

---

## 📊 Results
- **Accuracy:** ~80–85% (may vary slightly depending on train-test split)
- **Key Insight:**  
  - Credit history and income strongly influence loan approval.
  - The model performs well in classifying approvals and rejections.

---

## 🚀 How to Run
1. Clone the repository or download the notebook.
2. Install dependencies:
   ```bash
   pip install numpy pandas seaborn scikit-learn
