# 🩺 Health Analytics with Machine Learning (Regression + Classification using Scikit-learn & Scratch Models)

This repository includes two machine learning projects aligned with **UN SDG Goal 3: Good Health and Well-being**.

---
## 📚 Table of Contents

- [📈 Life Expectancy Prediction (Regression)](#-life-expectancy-prediction-using-regression-models)
- [❤️ Heart Disease Prediction (Classification)](#️-heart-disease-prediction-classification-task)

## 📁 Project 1: Life Expectancy Prediction (Regression)

### 📊 Dataset
- **Source**: Kaggle
- **Features**: Adult Mortality, HIV/AIDS, Income Composition, BMI, Schooling, etc.
- **Target**: Life Expectancy

### 🔍 EDA Highlights
- Missing values filled using median.
- Strong negative correlation between **Adult Mortality** and **Life Expectancy**.
- Left-skewed target distribution.

### 🤖 Models & Performance
| Model               | RMSE | MAE  | R²   |
|---------------------|------|------|------|
| Linear Regression   | 4.22 | 3.17 | 0.81 |
| Random Forest       | 2.10 | 1.26 | 0.95 |

### 🔧 Tuning & Features
- **Best RF Params**: `n_estimators=100`, `max_depth=10`, etc.
- **Top 3 Features (RF)**: Adult Mortality, HIV/AIDS, Income Composition

### ✅ Final RF Model
- High accuracy with only 3 features
- RMSE ≈ 2.10, R² ≈ 0.94

---

## 🫀 Project 2: Heart Disease Prediction (Classification)

### 📊 Dataset
- **Source**: [Kaggle - Heart Disease UCI](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)
- **Target**: HeartDisease (1 = Yes, 0 = No)
- **Features**: Age, ChestPainType, Cholesterol, MaxHR, Oldpeak, etc.

### 🔍 EDA Insights
- No missing values
- Important indicators: ST_Slope, ExerciseAngina, Oldpeak

### 🧮 Logistic Regression (from scratch)
- Train Acc: 84%, Test Acc: 82%

### 🤖 Sklearn Models
| Model                | Accuracy | Precision | Recall | F1-Score |
|----------------------|----------|-----------|--------|----------|
| Random Forest        | **89%**  | 0.92      | 0.90   | 0.91     |
| Gradient Boosting    | 86%      | 0.91      | 0.84   | 0.88     |

### 🔧 Tuning & Features
- **Best RF Params**: `n_estimators=100`, `max_depth=10`, etc.
- **Selected Features (6 total)**: ChestPainType, Cholesterol, MaxHR, Oldpeak, ST_Slope, etc.

---

## 🧾 Conclusion

- **Best Models**:
  - Regression: ✅ Random Forest (Life Expectancy)
  - Classification: ✅ Random Forest (Heart Disease)
- **Impact**:
  - Feature selection reduced dimensionality by ~45%.
  - Hyperparameter tuning improved generalization & efficiency.

---
## 📚 Requirements

- Python 3.x  
- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- seaborn  
