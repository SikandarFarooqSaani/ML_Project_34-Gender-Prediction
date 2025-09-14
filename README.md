# 👨‍🦰👩 Gender Classification using Machine Learning

![Gender Classification Banner](https://cdn-icons-png.flaticon.com/512/1034/1034155.png)

## 📌 Project Overview
This project focuses on predicting **gender classification** using a dataset from Kaggle.  
The dataset contains **7 features** and is completely **balanced** between male and female classes.  
The goal was to compare different machine learning models and find the best-performing one.

📂 **Dataset Link:** [Kaggle - Gender Classification Dataset](https://www.kaggle.com/datasets/elakiricoder/gender-classification-dataset)

---

## 📊 Dataset Details
- **Shape:** (5001, 8) → 5001 rows × 8 columns  
- **Target Column:** `gender` (encoded as **0 = Male, 1 = Female**)  
- **Balance:**  
  - Male (0): 2501  
  - Female (1): 2500  
- **Duplicates:** 1768 rows (handled during preprocessing)  
- **Missing Values:** None  

---

## ⚙️ Models and Results

### 1️⃣ Logistic Regression
- Accuracy: **0.960**  
- Errors: 23 FN, 17 FP  
- ![Confusion Matrix 1]
- <img width="649" height="547" alt="34-1" src="https://github.com/user-attachments/assets/f4064698-e643-41d2-822e-c273f36c8d98" />



---

### 2️⃣ Random Forest
- Accuracy: **0.950**  
- Errors: 22 FN, 19 FP  

---

### 3️⃣ Decision Tree
- Accuracy: **0.950**  
- Errors: 26 FN, 22 FP  
- <img width="649" height="547" alt="34-2" src="https://github.com/user-attachments/assets/9d856d5b-80d8-43e1-ae7d-aee8c800e35d" />



---

### 4️⃣ K-Nearest Neighbors (KNN)
- Accuracy: **0.962**  
- Errors: 27 FN, 11 FP  
- !<img width="649" height="547" alt="34-3" src="https://github.com/user-attachments/assets/55ad5d40-c278-432c-a33b-17bcfaacee9f" />


---

### 5️⃣ Support Vector Classifier (SVC)
- Accuracy: **0.963**  
- Errors: 21 FN, 16 FP  
- ![Confusion Matrix 4]
- <img width="649" height="547" alt="34-4" src="https://github.com/user-attachments/assets/55da59df-42c0-4f9c-bd43-e45804f1fde2" />


---

### 6️⃣ AdaBoost
- Accuracy: **0.962**  
- Errors: 20 FN, 18 FP  
- <<img width="649" height="547" alt="34-5" src="https://github.com/user-attachments/assets/97350f42-1abd-46db-9465-54977d26ee27" />



---

### 7️⃣ Gradient Boosting (GB)
- Accuracy: **0.967** 🎯  
- Errors: 23 FN, 10 FP  
- <img width="649" height="547" alt="34-6" src="https://github.com/user-attachments/assets/ed2d2d20-42a9-4a4e-8342-a93d0770bced" />


---

### 8️⃣ Stacking Classifier  
(Base Models: RF, GB, SVC, DT, LR | Meta Model: KNN)  
- Accuracy: **0.972** 🚀 (Best)  
- Errors: 20 FN, 8 FP  
- <img width="649" height="547" alt="34-7" src="https://github.com/user-attachments/assets/39dbf799-b863-49f6-8396-3f1b717c651e" />


---

## 🏁 Key Takeaways
- **Gradient Boosting** stood out among individual models with **96.7% accuracy**.  
- **Stacking Classifier** further improved performance to **97.2% accuracy** with minimal errors.  
- Dataset balance helped models achieve high accuracy without needing resampling or class weights.  
- Logistic Regression was surprisingly strong (96%), proving linear models can work well on structured datasets.  

---

## 📸 Visuals
All confusion matrices and comparison plots are included in this repo for clarity:
- CM for Logistic Regression, Decision Tree, KNN, SVC, AdaBoost, Gradient Boosting
- CM for **Stacking Classifier** (best model)

---

## 🙌 Conclusion
This project demonstrates that:  
- Ensemble methods like **Gradient Boosting** and **Stacking** can push accuracy beyond standard models.  
- Even on balanced datasets, **meta-learning with stacking** captures hidden patterns better.  
- Final best-performing model:  
  - **Stacking Classifier (RF + GB + SVC + DT + LR → KNN meta)**  
  - **Accuracy: 0.972** 🎉  

---
