# 🚀 Real-Time Fraud Detection System Using Machine Learning

> An end-to-end machine learning pipeline for real-time financial fraud detection using behavioral feature engineering and ensemble learning techniques.

<p align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-Gradient%20Boosting-green)
![License](https://img.shields.io/badge/License-MIT-success)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

</p>

---

# 📌 Project Overview

Financial fraud remains one of the biggest challenges facing modern banking systems, resulting in billions of dollars in annual losses. Detecting fraudulent transactions accurately while minimizing false alarms is essential for protecting both financial institutions and customers.

This project presents a complete **end-to-end machine learning pipeline** for detecting fraudulent financial transactions using transaction characteristics, behavioral feature engineering, and supervised machine learning algorithms.

Unlike many fraud detection implementations, this project explicitly identifies and removes **target leakage**, ensuring that every model is trained only on information available **before transaction authorization**, making the final solution suitable for real-time fraud detection.

---

# 🎯 Project Objectives

The objectives of this project are to:

- Develop an end-to-end fraud detection pipeline.
- Perform comprehensive Exploratory Data Analysis (EDA).
- Engineer meaningful behavioral features.
- Detect and eliminate target leakage.
- Train multiple machine learning models.
- Compare model performance using appropriate evaluation metrics.
- Recommend the best model for real-time fraud detection.

---

# 📊 Dataset

The project uses a simulated financial transaction dataset containing both legitimate and fraudulent transactions.

### Target Variable

- **isFraud**

### Available Features

- Transaction Type
- Transaction Amount
- Sender Balance
- Receiver Balance
- Transaction Time
- Customer / Merchant Information

---

# ⚙️ Machine Learning Workflow

```
Raw Dataset
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Feature Engineering
      │
      ▼
Target Leakage Detection & Removal
      │
      ▼
Train-Test Split
      │
      ▼
Preprocessing Pipeline
      │
      ▼
Logistic Regression
      │
      ▼
Random Forest
      │
      ▼
XGBoost
      │
      ▼
Model Evaluation
      │
      ▼
Model Comparison
      │
      ▼
Final Model Selection
```

---

# 📈 Exploratory Data Analysis

The exploratory analysis revealed several important fraud patterns.

### Key Findings

- Fraud is extremely rare, resulting in a highly imbalanced classification problem.
- Fraudulent transactions primarily occur through **TRANSFER** and **CASH_OUT** transaction types.
- Fraudulent transactions generally involve larger transaction amounts.
- Fraudsters frequently attempt to transfer nearly the entire available account balance.
- Transaction timing contributes useful predictive information.

---

# 🧠 Feature Engineering

Several domain-inspired features were engineered to improve fraud detection performance.

### Engineered Features

- High Balance Utilization
- Destination Customer Indicator
- Hour of Day
- Day of Month

Additional engineered variables were initially explored. During model development, features relying on **post-transaction account balances** were identified as introducing target leakage and were removed to ensure realistic model evaluation and real-time applicability.

---

# 🤖 Machine Learning Models

Three supervised learning algorithms were evaluated.

| Model | Purpose |
|--------|----------|
| Logistic Regression | Baseline interpretable model |
| Random Forest | Ensemble learning benchmark |
| XGBoost | Final optimized model |

---

#  Model Performance

| Model | Precision | Recall | F1-score | ROC-AUC | PR-AUC |
|--------|----------:|-------:|---------:|--------:|--------:|
| Logistic Regression | **1.00** | 0.11 | 0.19 | 0.9657 | *(Update with final value)* |
| Random Forest | 0.97 | 0.58 | 0.73 | 0.9681 | 0.8076 |
|  **XGBoost** | **0.92** | **0.69** | **0.79** | **0.9988** | **0.8602** |

---

#  Final Model

Among the evaluated algorithms, **XGBoost** achieved the strongest overall performance.

### Final Performance

- Precision: **92%**
- Recall: **69%**
- F1-score: **0.79**
- ROC-AUC: **0.9988**
- PR-AUC: **0.8602**

These results demonstrate that XGBoost provides the best balance between fraud detection capability and minimizing false alarms, making it the recommended model for real-time fraud detection.

---

#  Project Highlights

- ✅ End-to-End Machine Learning Pipeline
- ✅ Comprehensive Exploratory Data Analysis
- ✅ Domain-Driven Feature Engineering
- ✅ Target Leakage Detection and Removal
- ✅ Pipeline-Based Data Preprocessing
- ✅ Logistic Regression Baseline
- ✅ Random Forest Ensemble Model
- ✅ XGBoost Optimization
- ✅ Comprehensive Model Comparison
- ✅ Business-Oriented Model Evaluation

---

# 📁 Repository Structure

```
Real-Time-Fraud-Detection-System/

├── notebooks/
│   └── 01_Fraud_Detection_End_to_End.ipynb
│
├── data/
│   ├── raw/
│   └── processed/
│
├── figures/
│
├── models/
│
├── results/
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

#  Future Improvements

Potential future enhancements include:

- Hyperparameter optimization using Optuna
- Model explainability using SHAP
- Real-time deployment with FastAPI
- Docker containerization
- Streaming fraud detection
- Cost-sensitive learning
- Explainable AI (XAI)
- MLOps pipeline and model monitoring

---

# 👨‍💻 About the Author

**Razan Abdullah**

statistics + computer science graduate
University of Khartoum

**Areas of Interest**

- Data Science
- Machine Learning
- Artificial Intelligence
- Predictive Analytics
- Research Engineering

---

#  Acknowledgements

This project was developed as part of a comprehensive machine learning portfolio focused on solving real-world financial fraud detection problems using modern data science methodologies.

If you found this project interesting, consider giving it a ⭐ on GitHub.
