# Insurance Dataset - EDA, Preprocessing & Feature Engineering

This mini project focuses on performing **Exploratory Data Analysis (EDA)** and building a complete **data preprocessing pipeline** on the **Insurance dataset** to prepare it for Machine Learning model training.

---

## 📌 Project Objectives
- Understand the dataset using EDA
- Clean and preprocess the dataset
- Convert categorical data into machine-readable format
- Perform feature engineering
- Scale numeric features
- Select important features using statistical methods
- Create a final ML-ready dataset

---

## 📂 Dataset
- **File name:** `insurance.csv`
- **Target column:** `charges` (medical insurance cost)

---

## ✅ Work Done in This Notebook

### 1️⃣ Exploratory Data Analysis (EDA)
- Checked dataset shape, columns, datatypes
- Verified missing values and basic statistics
- Visualized numeric distributions:
  - `age`, `bmi`, `children`, `charges`
- Visualized categorical distributions:
  - `smoker`
- Generated correlation heatmap

---

### 2️⃣ Data Cleaning & Preprocessing
- Copied the original dataset for safe operations
- Removed duplicate records
- Converted categorical columns to numeric:
  - `sex` → `is_female` (male=0, female=1)
  - `smoker` → `is_smoker` (no=0, yes=1)
- Applied **One-Hot Encoding** on `region`

---

### 3️⃣ Feature Engineering
- Created BMI categories using `pd.cut()`:
  - Underweight
  - Normal
  - Overweight
  - Obese
- One-hot encoded BMI categories

---

### 4️⃣ Feature Scaling
- Standardized numeric features using **StandardScaler**
  - `age`, `bmi`, `children`

---

### 5️⃣ Feature Extraction / Selection
- **Pearson Correlation**
  - to analyze relationship of features with `charges`
- **Chi-Square Test**
  - applied on categorical variables (charges converted into bins)

---

### 6️⃣ Final Dataset Creation
Created the final dataset with selected features:
- `age`
- `is_female`
- `bmi`
- `children`
- `is_smoker`
- `region_southeast`
- `bmi_category_Obese`
- **Target:** `charges`

---

## 🛠️ Libraries Used
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `scipy`

---

## 📌 Output
✅ Final clean & processed dataframe: `final_df`  
This dataset can now be directly used to train ML models like:
- Linear Regression
- Random Forest Regressor
- XGBoost Regressor

---


