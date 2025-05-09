# 🍷 Wine Quality Prediction (Red Wine)

Welcome to my Machine Learning project on predicting the quality of red wine using physicochemical properties from the popular Wine Quality dataset by [Cortez et al., 2009].

---

## 📌 Project Summary

This is my **second attempt** at this project. In my first attempt, the model accuracy reached **0.77**. After improving data handling, feature engineering, and modeling, I achieved **91% accuracy** with Random Forest.

---

## 📂 Dataset Overview

- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/wine+quality)
- **Type**: Red wine quality data (Vinho Verde, Portugal)
- **Features**: 11 physicochemical inputs
- **Target**: Quality score (0–10), converted into binary class (Good / Bad)

---

## ⚙️ Techniques Used

### 🔍 Exploratory Data Analysis (EDA)
- Used `heatmap`, `histogram`, and `pairplot` to visualize patterns and feature relationships.
- Identified strong correlation between **alcohol**, **sulphates**, and **quality**.

### 🚫 Outlier Handling
- Manually removed a **small number of outliers** in:
  - `sulphates`
  - `residual sugar`
  - `total sulfur dioxide`
- Kept most data to retain learning potential.

### 🧪 Feature Engineering
- Created binary labels:  
  `quality >= 7 → Good (1)`  
  `quality < 7 → Bad (0)`
- Added new features:
  - `alcohol × sulphates`
  - `density × pH`
  - `acid_sum = fixed + volatile + citric acid`

### 🤖 Modeling
- Trained and evaluated:
  - `Logistic Regression`
  - `Random Forest Classifier`

---

## 📈 Model Performance

### 🔹 Logistic Regression
- **Accuracy**: `0.8415`

### 🔹 Random Forest Classifier
- **Accuracy**: `0.9101`
- **Confusion Matrix**:
  ```
  [[195  32]
   [ 10 230]]
  ```
- **Precision/Recall/F1**: High for both classes

---

## 🗂️ Project Structure

```
📦 winequality-red
 ┣ 📂csv_files
 ┃ ┗ 📜 winequality-red.csv
 ┣ 📂pkl_models
 ┃ ┣ 📜 logistic_regression_model.pkl
 ┃ ┗ 📜 random_forest_model.pkl 
 ┗ 📜 Notebook.ipynb
```

---

## 👨‍💻 Author

**Yahan Madhuhansa**



