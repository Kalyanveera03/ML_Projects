# Credit Card Fraud Detection

A machine learning project that uses Logistic Regression to detect fraudulent credit card transactions. This project addresses the challenge of highly imbalanced datasets through undersampling techniques.

## 📊 Project Overview

Credit card fraud detection is a critical application of machine learning in the financial sector. This project builds a binary classification model to identify fraudulent transactions from a dataset of credit card transactions.

### Key Features
- Handles imbalanced dataset using undersampling
- Achieves ~94.8% accuracy on training data
- Achieves ~90.9% accuracy on test data
- Uses Logistic Regression for classification

## 📁 Dataset

The dataset contains credit card transactions with the following characteristics:
- **Total Transactions**: 284,807
- **Fraudulent Transactions**: 492 (0.17%)
- **Legitimate Transactions**: 284,315 (99.83%)
- **Features**: 30 anonymized features (V1-V28) + Time + Amount
- **Target**: Class (0 = Legitimate, 1 = Fraud)

### Dataset Structure
- `Time`: Seconds elapsed between transactions
- `V1-V28`: PCA-transformed features (anonymized for confidentiality)
- `Amount`: Transaction amount
- `Class`: Target variable (0 or 1)

## 🔧 Technologies Used

- **Python 3.x**
- **NumPy**: Numerical computations
- **Pandas**: Data manipulation and analysis
- **Scikit-learn**: Machine learning algorithms and metrics
  - Logistic Regression
  - Train-test split
  - Accuracy score

## 🚀 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/credit-card-fraud-detection.git
cd credit-card-fraud-detection
```

2. Install required packages:
```bash
pip install numpy pandas scikit-learn
```

3. Download the dataset (creditcard.csv) and place it in the project directory.

## 💻 Usage

1. Open the Jupyter notebook or run the Python script:
```bash
jupyter notebook creditcard_fraud.ipynb
```

2. The workflow includes:
   - Loading and exploring the data
   - Analyzing class distribution
   - Creating a balanced dataset using undersampling
   - Splitting data into training and testing sets
   - Training a Logistic Regression model
   - Evaluating model performance

## 📈 Methodology

### 1. Data Exploration
- Checked for missing values (none found)
- Analyzed class distribution
- Compared statistical measures between legitimate and fraudulent transactions

### 2. Handling Imbalanced Data
Used **undersampling** technique:
- Randomly sampled 492 legitimate transactions
- Combined with all 492 fraudulent transactions
- Created a balanced dataset of 984 samples (50% fraud, 50% legitimate)

### 3. Model Training
- Algorithm: **Logistic Regression**
- Train-test split: 80-20 ratio with stratification
- Training samples: 787
- Testing samples: 197

## 📊 Results

| Metric | Training Data | Test Data |
|--------|--------------|-----------|
| Accuracy | 94.79% | 90.86% |

## 🔍 Key Insights

1. **Class Imbalance**: The original dataset is highly imbalanced (99.83% legitimate vs 0.17% fraud)
2. **Feature Engineering**: The V1-V28 features are already PCA-transformed
3. **Transaction Amount**: Fraudulent transactions show slightly higher average amounts ($122.21) compared to legitimate ones ($88.29)
4. **Model Performance**: The model shows good generalization with consistent performance on both training and test data

## ⚠️ Limitations

- Undersampling may result in loss of information from legitimate transactions
- Model trained on a relatively small balanced dataset (984 samples)
- May not capture all fraud patterns present in the complete dataset

## 🙏 Acknowledgments

- Dataset source: [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Inspired by real-world fraud detection challenges in the financial industry

---

⭐ If you found this project helpful, please consider giving it a star!
