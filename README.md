# 365-Day Hospital Readmission Prediction for Ischemic Stroke

## Repository Overview

This repository presents an end-to-end machine learning pipeline for predicting
365-day hospital readmission among patients diagnosed with ischemic stroke.
The study leverages the MIMIC-IV clinical database and evaluates multiple machine
learning models to assess predictive performance and identify clinically relevant
features.

---

## Repository Contents

1. Team Contract – [`ML4Health_TeamContract_17.pdf`](ML4Health_TeamContract_17.pdf)  
2. Project Proposal – [`ML4Health_proposal_Group17.pdf`](ML4Health_proposal_Group17.pdf)  
3. Cohort Extraction and Exploratory Data Analysis – [`Data_Handling.ipynb`](Data_Handling.ipynb)  
4. Generic Data Processing Pipeline – [`Process_Data_Generic.ipynb`](Process_Data_Generic.ipynb)  
5. Machine Learning Modelling – [`ML_Models.ipynb`](ML_Models.ipynb)  
6. Feature Importance Analysis – [`Feature_Importance_ISP_Dataset.ipynb`](Feature_Importance_ISP_Dataset.ipynb)  
7. Pre-processed Full Cohort Dataset – [`full_cohort.csv`](full_cohort.csv)  
8. Environment and Dependency Requirements – [`requirements.txt`](requirements.txt)

---

## Objective

The objective of this study is to predict 365-day hospital readmission for patients
admitted with ischemic stroke and to identify key predictive clinical features that
may inform clinical decision-making and post-discharge risk stratification.

---

## Materials and Methods

### Dataset
- MIMIC-IV (version 2.2)
- Adult patients diagnosed with ischemic stroke

### Machine Learning Models
- Random Forest
- XGBoost
- PCA-based Clustering

### Methodology
- Class imbalance in readmission outcomes was addressed using SMOTE oversampling
  for the Random Forest model.
- Hyperparameters were optimized using grid search with cross-validation.
- Model performance was evaluated using AUC-ROC and additional classification metrics.
- Feature importance was examined using permutation importance and PCA-based
  clustering techniques.

---

## Results

- Random Forest achieved an AUC of 0.64.
- XGBoost achieved an AUC of 0.78.

Overall predictive performance was moderate, indicating limited discriminative
ability despite the use of imbalance correction techniques.

### Key Predictive Features
- Length of hospital stay
- Troponin T levels
- Maximum systolic blood pressure

Feature importance analyses suggest complex, non-linear interactions among
clinical variables contributing to readmission risk.

---

## How to Run the Code

### Step 1: Obtain Access to MIMIC-IV
Access to the MIMIC-IV database and BigQuery setup is required.
Instructions are available at:
[https://physionet.org/content/mimiciv/2.2/](https://physionet.org/content/mimiciv/2.2/)

### Step 2: Environment Setup
Install the required dependencies using:
```bash
pip install -r requirements.txt
```

### Step 3: Cohort Extraction and Exploratory Data Analysis

Run [`Data_Handling.ipynb`](Data_Handling.ipynb) to extract the ischemic stroke cohort and perform
exploratory data analysis.  
Alternatively, the pre-processed dataset [`full_cohort.csv`](full_cohort.csv) may be used directly.

### Step 4: Model Training and Evaluation

Execute [`ML_Models.ipynb`](ML_Models.ipynb) to perform data preprocessing, model training,
model evaluation, and performance analysis.

### Step 5: Feature Importance Analysis

Run [`Feature_Importance_ISP_Dataset.ipynb`](Feature_Importance_ISP_Dataset.ipynb) to analyze feature contributions
to model predictions.

---

## Conclusion

This study highlights the challenges associated with predicting hospital
readmission using real-world clinical data. Constructing a clinically relevant,
sufficiently large, and complete ischemic stroke cohort proved challenging.
The moderate performance observed across models is consistent with existing
literature, suggesting that 365-day stroke readmission prediction remains a
complex and difficult task even with advanced machine learning techniques.

---

Group 17