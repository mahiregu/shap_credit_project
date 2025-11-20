# SHAP Credit Risk Prediction Project

This project builds a credit risk prediction model using **XGBoost** and explains its decisions using **SHAP (SHapley Additive exPlanations)**.  
It demonstrates both global and local interpretability for loan applicant risk analysis.
---
## 📂 Project Structure
```
shap_credit_project/
│
├── global_shap_analysis.txt
├──local_case_explanations.txt
├── model_performance.txt
├── shap_credit_project.ipynb
└── submission_markdown.md

```

---

## 📌 File Descriptions

### **1. shap_credit_project.ipynb**  
This is the full Google Colab notebook containing:
- Synthetic dataset creation  
- Preprocessing pipeline  
- XGBoost model training  
- Hyperparameter tuning  
- SHAP global feature importance  
- SHAP local explanations for 3 individuals  
- All plots and outputs  

This file shows the *complete implementation*.

---

### **2. model_performance.txt**  
Contains the test-set evaluation metrics:
- AUC  
- Precision  
- Recall  
- F1-Score  
- Accuracy  

These metrics summarize the final model’s performance.

---

### **3. global_shap_analysis.txt**  
A written explanation of the **global** SHAP results:
- Top 3 most important features  
- How each feature influences credit risk  
- Interpretation of the SHAP summary plot  

Shows understanding of model interpretability.

---

### **4. local_case_explanations.txt**  
Contains **local SHAP explanations** for 3 sample applicants:
- One high-risk prediction  
- One medium-risk prediction  
- One low-risk prediction  

Explains why each person received their specific risk score.

---

### **5. submission_markdown.md**  
A complete, combined report ready to be submitted on your course website:
- Model performance  
- Global SHAP summary  
- Local explanations  
- Final remarks  

Useful for copy-paste submissions.

---

## 🎯 Project Goal

To build a transparent credit risk model that:
- Predicts whether an applicant is likely to default  
- Explains *why* the model gives a particular prediction  
- Demonstrates responsible and interpretable AI practice  

---

## 🛠 Tools Used
- Python  
- Google Colab  
- Scikit-learn  
- XGBoost  
- SHAP  
- Pandas, NumPy, Matplotlib  

---

## ⭐ Summary

This project combines machine learning with explainability to show:
- **How** a credit risk model works  
- **Which features** drive risk  
- **Why** individual applicants receive certain risk scores  

It is designed to meet academic requirements for an interpretable ML project.



