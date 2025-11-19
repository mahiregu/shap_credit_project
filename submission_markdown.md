# Credit Risk Prediction Using XGBoost and SHAP  
### Final Submission Report

---

## 1. Project Overview

This project builds a credit default prediction model using the XGBoost classifier.  
To ensure interpretability, SHAP (SHapley Additive exPlanations) is used to explain both global and local model behavior.  

The goal is to understand:
- How the model predicts default risk  
- Which features influence the predictions the most  
- Why specific applicants receive their assigned risk scores  

The project uses a synthetic credit dataset created in Google Colab.

---

## 2. Model Performance Summary

Test metrics (provided from notebook execution):

- **AUC:** 0.7877  
- **Precision:** 0.6667  
- **Recall:** 0.4333  
- **F1 Score:** 0.5253  
- **Accuracy:** 0.77  

**Classification Report:**

                 precision    recall  f1-score   support
Class 0           0.79       0.91      0.84       140
Class 1           0.67       0.43      0.53        60

Overall Accuracy: 0.77
Macro Avg:        0.73       0.67      0.68       200
Weighted Avg:     0.75       0.77      0.75       200


**Interpretation**  
- The model performs well for non-defaulters (class 0).  
- Class 1 (defaulters) has lower recall (0.43), meaning some risky applicants are missed — common in imbalanced datasets.  
- The AUC of 0.7877 indicates good overall discriminative performance.

---

## 3. Global SHAP Analysis

The SHAP global importance scores show the features that influence predictions across all customers.

**Top Three Risk Drivers:**
1. **checking_status_no_checking**  
2. **duration**  
3. **credit_amount**  

### Summary of Their Influence:

- **checking_status_no_checking:**  
  The strongest predictor of default. Having no checking account is linked to higher financial risk.

- **duration:**  
  Long loan durations increase uncertainty and push risk upward.

- **credit_amount:**  
  Large credit amounts increase the financial burden and raise default likelihood.

These top three features dominate the model’s decision-making, and the pattern is consistent with real-world financial logic.

---

## 4. Local SHAP Explanations (Three Individuals)

### **Applicant 1 – High Risk**
Prediction was high because:
- No checking account (largest positive contributor)  
- High loan amount  
- Long duration  
- Negative credit history  

Combined, these factors pushed the SHAP value strongly upward.

---

### **Applicant 2 – Medium Risk**
Prediction was moderate because:
- Slightly long duration and medium credit amount increased risk  
- Low savings added vulnerability  
- But stable employment slightly reduced the score  

Risk-increasing and risk-lowering factors balanced each other.

---

### **Applicant 3 – Low Risk**
Prediction was low because:
- Strong checking account balance  
- Short loan duration  
- Small credit amount  
- Good credit history  

These features pushed the SHAP value strongly downward, lowering risk.

---

## 5. Final Remarks

- The model performs reliably for a synthetic dataset.  
- SHAP provides clear explanations for both global and individual predictions.  
- The key factors the model focuses on are meaningful, interpretable, and aligned with real-world credit assessment practices.  
- This ensures transparency, which is essential in financial machine learning applications.

---


