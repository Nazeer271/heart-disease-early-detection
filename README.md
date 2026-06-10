# ❤️ Heart Disease Early Detection

Early detection of cardiovascular disease using machine learning classification models.

## 📌 Overview

Cardiovascular diseases are the leading cause of death worldwide. This project leverages machine learning to predict whether an individual is likely to have heart disease based on health indicators such as age, blood pressure, cholesterol levels, and lifestyle habits like smoking and alcohol consumption.

## 🎯 Problem Statement

Given a dataset of patient health records, predict the presence of heart disease using the binary target variable `disease`:
- **1** → Heart disease present
- **0** → No heart disease

## 📂 Project Structure

```
heart-disease-early-detection/
│
├── heart_disease_prediction.ipynb    # Main notebook
├── data/
│   └── Data_file.csv                 # Dataset
├── README.md
└── requirements.txt
```

## 🔧 Tech Stack

- Python 3.x
- pandas, numpy
- scikit-learn
- matplotlib, seaborn
- Jupyter Notebook

## 📊 Workflow

1. **Exploratory Data Analysis (EDA)** — Variable distributions, missing data checks, feature-target relationships
2. **Data Preprocessing** — Blood pressure outlier filtering, normalization with StandardScaler, feature engineering
3. **Model Development** — Four classifiers trained and compared:
   - Logistic Regression
   - Decision Tree
   - SVM (Linear)
   - Random Forest
4. **Model Evaluation** — Accuracy, Precision, Recall, F1-Score, Confusion Matrix
5. **Insights & Conclusion** — Most significant risk factors identified and reported

## ✅ Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Logistic Regression | 0.6250 | 0.5577 | 0.3580 | 0.4361 |
| Decision Tree | 0.5550 | 0.4500 | 0.4444 | 0.4472 |
| SVM (Linear) | 0.6200 | 0.5472 | 0.3580 | 0.4328 |
| **Random Forest** ✅ | **0.6500** | **0.5902** | **0.4444** | **0.5070** |

> **Selected Model: Random Forest** — Best accuracy (65.00%), highest precision (59.02%), and best F1-Score (0.5070).

### Key Risk Factors Identified
- **Systolic blood pressure (`ap_hi`)** — Strongest predictor; values above 140 mmHg significantly raise disease risk
- **Cholesterol levels** — High cholesterol (level 3) correlates strongly with disease presence
- **Age** — Risk increases notably after age 50
- **Physical activity** — Active individuals show measurably lower disease probability
- **Smoking** — Positive correlation with disease presence

## 🚀 Getting Started

```bash
git clone https://github.com/your-username/heart-disease-early-detection.git
cd heart-disease-early-detection
pip install -r requirements.txt
jupyter notebook heart_disease_prediction.ipynb
```

## 📋 Guidelines

- Data split: 80% training / 20% testing
- Blood pressure outliers filtered (ap_hi: 50–250 mmHg, ap_lo: 30–200 mmHg)
- All steps thoroughly documented in the notebook
- Final model balances accuracy with clinical interpretability
