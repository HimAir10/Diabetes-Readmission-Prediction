# 🩺 Implementation of Machine Learning Algorithms for Predicting Diabetic Patient Readmission
*A research-based implementation focusing on predicting hospital readmissions among diabetic patients using classical machine learning algorithms.*

## 📘 Overview  
This project implements multiple machine learning algorithms to predict whether diabetic patients are likely to be readmitted within **30 days** of discharge.  
The analysis is based on patient claims data collected from **1999–2008** in the United States.  
The goal is to identify risk factors and improve hospital management by reducing avoidable readmissions.

---

## 🧩 Dataset Source
The dataset used in this project is derived from the **UCI Machine Learning Repository – Diabetes 130-US hospitals for years 1999–2008 dataset**.
[Dataset Link](https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008)
## 🎯 Objective  
To develop an accurate and interpretable ML model that predicts diabetic patient readmission, enabling proactive healthcare interventions and optimized resource allocation.

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing  
- Handled missing and invalid values  
- Removed redundant columns (`weight`, `payer_code`, etc.)  
- Encoded categorical variables using one-hot encoding  
- Balanced classes using **SMOTE**  

### 2️⃣ Feature Engineering  
- Created new variables like **service utilization** and **numchange**  
- Grouped diagnostic codes into categories  
- Performed **Lasso Regression** for feature selection  

### 3️⃣ Exploratory Data Analysis (EDA)  
- Generated **heatmaps**, **scatter plots**, and **density plots**  
- Analyzed relationships between diagnoses, medications, and readmission  

### 4️⃣ Modeling  
Implemented and evaluated:  
- Linear Discriminant Analysis (LDA)  
- Random Forest  
- Support Vector Machine (SVM)  
- K-Nearest Neighbors (KNN)  
- Naïve Bayes  

Evaluation was done using **5-fold cross-validation** with metrics such as **Accuracy**, **Precision**, **Recall**, **F1-Score**, and **AUC**.

---

## 📊 Results & Analysis  
The models were evaluated using 5-fold cross-validation on the diabetic dataset.

Random Forest achieved the best overall performance with accuracy = 0.8719 and AUC = 0.5854, showing strong generalization.
Naïve Bayes recorded lower accuracy (0.5818) but the highest recall = 0.4321, useful for identifying actual readmissions.
LDA and SVM performed similarly (accuracy = 0.8169, AUC ≈ 0.53), while KNN achieved accuracy = 0.8140.

Overall, **Random Forest** emerged as the most reliable and balanced model, whereas Naïve Bayes offered greater sensitivity for medical prediction tasks.

---

## 🧠 Technologies Used
- **Language:** Python 3.10+  
- **Environment:** Google Colab  
- **Libraries:**  
  - pandas, numpy, seaborn, matplotlib  
  - scikit-learn  
  - imbalanced-learn (SMOTE)  

---

## 🚀 How to Run the Project

### Option 1: Run on Google Colab  
1. Open [Google Colab](https://colab.research.google.com/).  
2. Upload `Final_Model.ipynb`.  
3. Mount your dataset (`diabetic_data.csv`).  
4. Run all cells sequentially.

### Option 2: Run Locally  
```bash
git clone https://github.com/Anushka1590/diabetic-readmission-prediction.git
cd diabetic-readmission-prediction
jupyter notebook Final_Model.ipynb
```

---

## 🩹 Future Scope  
- Incorporate deep learning techniques for improved prediction.  
- Expand the dataset for multi-hospital generalization.  
- Develop a web or mobile interface for clinical use.  

---

## 📜 License  
This project is licensed under the **MIT License** — feel free to use and modify with attribution.

---


