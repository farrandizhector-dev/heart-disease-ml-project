# Heart Disease Prediction – Machine Learning Project

This project is part of my learning path as a junior data scientist.  
The goal was to build a complete, clean and well-structured machine learning pipeline using a real medical dataset (the Cleveland Heart Disease dataset from UCI).

Even though I am still 18 and in the early stages of my data science journey, I wanted to create a project that follows the structure and practices used in real-world ML work:  
data cleaning, EDA, preprocessing, model training, evaluation and documentation.

---

## 📁 Project Structure

Proyecto4_HeartDisease/
│
├── notebook.ipynb # Full ML workflow
├── heart.csv # Original Cleveland dataset (renamed to CSV)
├── plots/ # All EDA + evaluation graphs
└── README.md # Project documentation

---

## 📊 Dataset Overview

**Source:** Cleveland Heart Disease dataset (UCI Machine Learning Repository)  
**Rows:** 303  
**Columns:** 14  
**Task:** Binary classification (heart disease: yes/no)

The original target ranges from **0 to 4**, so I converted it into a binary variable:

- `0` → No heart disease  
- `1` → Heart disease present (original values 1–4)

This conversion is commonly used in research and ML projects.

---

## 🧹 Data Cleaning & Preprocessing

Steps completed:

1. Replaced missing values `"?"` with `NaN`.
2. Converted all features to numeric format.
3. Dropped rows with missing values (the dataset loses only a few).
4. Created a binary target variable.
5. Performed a **stratified train-test split** (to preserve class ratio).
6. Scaled features only for Logistic Regression.
7. Kept Random Forest unscaled (tree models don’t need scaling).

Even as a junior, my goal was to ensure data integrity and a reproducible workflow.

---

## 🔍 Exploratory Data Analysis (EDA)

Key visualizations (all saved in `/plots`):

- Heart disease distribution
- Histograms of all features
- Correlation heatmap
- Age vs Heart Disease boxplot

**Insights collected:**

- Patients with heart disease tend to be older on average.
- Important features include: `thalach`, `oldpeak`, `ca`, `cp`.
- The dataset is reasonably balanced after binarization.

---

## 🤖 Machine Learning Models

I trained and evaluated **two supervised classification models**:

### **1️⃣ Logistic Regression**
- Simple, explainable baseline
- Requires scaled features
- High AUC performance

### **2️⃣ Random Forest**
- Handles non-linear patterns
- No scaling required
- Slightly higher accuracy

Both models are trained following standard ML practices.

---

## 🧪 Model Performance

| Model                 | Accuracy | AUC  |
|----------------------|----------|------|
| Logistic Regression  | 0.8333   | 0.9498 |
| Random Forest        | 0.8667   | 0.9453 |

**Observations:**

- Logistic Regression has a **slightly better AUC**, meaning strong ranking ability.
- Random Forest achieves **higher accuracy**, showing strong classification performance.
- Both models generalize well and show no signs of overfitting.

Graphs such as ROC Curves and Confusion Matrices are saved in the `/plots` folder.

---

## 📈 Evaluation Plots

Saved automatically during the notebook execution:

- `target_distribution.png`
- `feature_histograms.png`
- `correlation_heatmap.png`
- `boxplot_age_target.png`
- `logistic_confusion_matrix.png`
- `logistic_roc_curve.png`
- `random_forest_confusion_matrix.png`
- `random_forest_roc_curve.png`

These diagrams help evaluate model behavior visually.

---

## 🚀 How to Run the Project

1. Clone or download this repository.
2. Install dependencies:

3. Open the `notebook.ipynb` in Jupyter Notebook or VS Code.
4. Run all cells in order (1 → 8).
5. All graphs will appear inside the notebook and will be saved in `/plots`.

---

## 🎯 What I Learned (as a junior data scientist)

This project helped me improve in:

- Understanding how real medical datasets behave  
- Cleaning and preparing data for ML  
- Creating meaningful visualizations  
- Training and comparing ML models  
- Evaluating performance using metrics and plots  
- Structuring a project like a real ML workflow  

My goal was to build something clean, readable and professional — and I feel this project reflects that.

---

## 👤 Author

Héctor Ferrándiz Sanchis]  
18  years old
**Role:** Junior Data Scientist  
**Project:** Machine Learning – Predicting Heart Disease  

Feel free to contact me if you want to give feedback or discuss improvements.

