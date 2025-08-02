# 🫀 Heart Disease Prediction using Logistic Regression

This project focuses on predicting the **10-year risk of Coronary Heart Disease (CHD)** using a Logistic Regression model trained on the **Framingham Heart Study dataset**. The pipeline includes data preprocessing, class imbalance handling with SMOTE, model training, evaluation, and prediction for new patient data.

## 🔍 Project Objective

- Predict the likelihood of CHD based on patient health metrics.
- Handle class imbalance to improve recall for CHD-positive cases.
- Enable individual predictions for new patients
  
## 📁 Dataset

- Source: [Framingham Heart Study dataset]
- File: `framingham.csv`
- Features include:
  - Demographics: Age, Gender
  - Lifestyle: Smoking, Cigarettes per day
  - Medical: BMI, BP, Cholesterol, Glucose, Diabetes
  - Target: `TenYearCHD` (0 = No Risk, 1 = CHD Risk)

## 🧰 Tech Stack

- **Python 3.9+**
- **Pandas**, **NumPy**
- **Seaborn**, **Matplotlib**
- **Scikit-learn**
- **Imbalanced-learn (SMOTE)**

## ⚙️ Project Workflow

### 1. Import Libraries and Load Dataset
- Load the CSV using `pandas`
- Drop irrelevant columns (e.g., `education`)
- Rename columns for readability

### 2. Data Preprocessing
- Remove rows with missing values
- Normalize numerical features using `StandardScaler`
- Use **SMOTE** to oversample the minority class (CHD = 1)
- Split data into training (70%) and testing (30%)

### 3. Exploratory Data Analysis (EDA)
- Class distribution check
- Histograms of key features
- Correlation heatmap
- Boxplots to analyze impact of risk factors

### 4. Model Training
- Train a `LogisticRegression` model on SMOTE-resampled data
- Use binary cross-entropy loss (built-in)

### 5. Model Evaluation
- Evaluate using:
  - Accuracy
  - Precision, Recall, F1-score
  - Confusion Matrix
  - ROC-AUC Score and Curve

### 6. Prediction for New Patients
- Input new patient data (as array)
- Predict probability and class (0 = low risk, 1 = high risk)

## 👩‍🔬 Acknowledgements
Framingham Heart Study

scikit-learn, imbalanced-learn
