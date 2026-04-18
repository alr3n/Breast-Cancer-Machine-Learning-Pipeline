# 🧠 Breast Cancer Classification using Machine Learning

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Machine Learning](https://img.shields.io/badge/ML-Scikit--Learn-orange.svg)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 📌 Project Overview
This project is a **Machine Learning classification system** that detects whether a breast tumor is **Benign (B)** or **Malignant (M)** using diagnostic features from biopsy data.

🎯 **Objective:** Build a highly reliable model focused on **minimizing False Negatives**, since missing a cancer case is critical in real-world medical diagnosis.

---

## 📊 Exploratory Data Analysis (EDA)

### 📈 Class Distribution
- 🟢 Benign: ~63%
- 🔴 Malignant: ~37%

📌 Insight: Slight imbalance but acceptable — no resampling required.

---

### 🌡️ Correlation Heatmap
- Strong correlations between:
  - radius
  - perimeter
  - area (≈ 0.99)

📌 Insight: These features are highly redundant but useful for tree-based models.

---

### 🔗 Pair Plot Analysis
- Clear class separation in:
  - radius_mean
  - perimeter_mean
  - area_mean

📌 Insight: These features are strong predictors of malignancy.

---

### 📦 Box Plot Analysis
- Malignant tumors show higher values in:
  - radius
  - perimeter
  - area

📌 Insight: These features are powerful classification signals.

---

## 🔍 Key Insights
✨ Malignant tumors are generally **larger and more irregular**  
✨ Concave points and concavity are strong malignancy indicators  
✨ Texture is a weak standalone feature  
✨ “Worst” features are the most predictive signals  

---

## 🧹 Data Preprocessing

### ❌ Removed Columns
- `id` → irrelevant identifier
- `Unnamed: 32` → empty artifact column

### 🔢 Encoding
- Malignant → 1
- Benign → 0

### ✂️ Train-Test Split
- 80% Training
- 20% Testing (Stratified)

### 📏 Feature Scaling
- StandardScaler applied
- Prevented data leakage (fit only on training set)

---

## 🤖 Machine Learning Models

### 📊 Logistic Regression
- Linear classifier
- Fast and interpretable
- Recall: **0.88**

---

### 🎯 Support Vector Machine (SVM - RBF)
- Maximizes decision margin
- Handles non-linear relationships
- Recall: **0.93**
- AUC: ~0.997

---

### 🌲 Random Forest 🏆
- Ensemble of decision trees
- Handles feature correlation well
- Feature importance available
- Accuracy: **97%**
- Recall: **0.93**
- Precision: **1.00**

---

## ⚙️ Model Optimization
- GridSearchCV used
- 5-Fold Cross Validation
- Optimized for **Recall (Cancer detection priority)**

📌 Goal: Reduce False Negatives as much as possible

---

## 📏 Evaluation Metrics

- 🎯 Accuracy → Overall correctness
- 🎯 Precision → Correct positive predictions
- ⭐ Recall → Detecting actual cancer cases (MOST IMPORTANT)
- ⚖️ F1-Score → Balance of Precision & Recall
- 📈 ROC-AUC → Model separability (~0.99 best models)

---

## 📊 Model Comparison

| Model                | Accuracy | Precision | Recall ⭐ | AUC   |
|---------------------|----------|-----------|----------|-------|
| Logistic Regression | 95%      | 0.93      | 0.88     | 0.99  |
| SVM (RBF) 🏆        | 97%      | 1.00      | 0.93     | 0.997 |
| Random Forest 🏆    | 97%      | 1.00      | 0.93     | 0.997 |

---


## 🧠 Key Takeaways
- Tumor size-related features are the strongest predictors
- “Worst” measurements outperform averages
- Feature scaling is essential for SVM & Logistic Regression
- Tree-based models handle correlated features effectively

---

## 🎯 Project Outcome
✔ 97% Accuracy  
✔ 93% Recall (Cancer detection rate)  
✔ High reliability for medical classification tasks  

⚠️ Designed with real-world priority: **minimizing missed cancer cases**

---

## 👨‍💻 Author
Replace with your name and links:
- GitHub: https://github.com/alr3n

---

⭐ If you like this project, consider giving it a star on GitHub!

