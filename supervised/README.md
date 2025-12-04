# Supervised Classification Model: Breast Cancer Diagnosis

# 📝 Description
This repository contains a Jupyter Notebook `supervised.ipynb` that implements a comprehensive supervised machine learning workflow for classifying breast cancer data. The project focuses on data exploration, feature analysis, model training using ensemble methods, and performance evaluation to accurately distinguish between benign (B) and malignant (M) diagnoses.

# 🎯 Project Goal
The primary goal is to develop and evaluate classification models, specifically focusing on AdaBoost and Gradient Boosting, to achieve high predictive accuracy for cancer diagnosis based on various cellular and nuclear features.

# 📊 Data Source
The analysis utilizes the Breast Cancer Wisconsin (Diagnostic) Dataset `cancer.csv`.

Feature Category,Description
Mean,The mean values of the 10 core features.
Standard Error,The standard error of the 10 core features.
Worst,"The ""worst"" or largest (mean of the three largest values) of the 10 core features."
Target Variable,"Diagnosis (Mapped: B = 0 for Benign, M = 1 for Malignant)."

# 🛠️ Methodology & Workflow
The notebook follows a standard data science methodology:

1-Data Loading and Preprocessing:
- The `cancer.csv` file is loaded.
- The categorical Diagnosis column is encoded numerically (B $\to$ 0, M $\to$ 1).
- The data is split into training and testing sets (test_size=0.2).
2-Exploratory Data Analysis (EDA) & Feature Engineering:
- Feature correlation and redundancy are explored using $R^2$ values between feature pairs.
- The code structure suggests the use of Principal Component Analysis (PCA) for dimensionality reduction (in the CancerAdaBoostPCA class).
3-Model Training:
- Ensemble learning models are trained and evaluated, including AdaBoost Classifier and Gradient Boosting Classifier.
4-Evaluation:
- Model performance is assessed using standard classification metrics: Accuracy, Precision, Recall, F1-Score, and ROC AUC.
- The workflow includes plotting Confusion Matrices and Learning Curves to visualize model behavior and stability.
# ✨Key Results
    Model           Cross-ValidationAccuracy    Best Test Accuracy
    Ada Boost               0.9319                    0.9386
    Gradient Boost          0.9319                    0.9298

Best Model: 
    Ada Boost achieved the highest overall accuracy of 0.9386 on the test set.
    Performance Metrics for AdaBoost (Test Set):
    Precision (Malignant): 0.93
    Recall (Malignant): 0.90
    F1-Score (Malignant): 0.92