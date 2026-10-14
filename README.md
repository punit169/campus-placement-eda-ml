# 📊 Census Income EDA & Machine Learning Classification
### IT462 Course Project 

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)](https://scikit-learn.org/)
[![Dataset](https://img.shields.io/badge/UCI-Adult_Census_Income-brightgreen.svg)](https://archive.ics.uci.edu/dataset/2/adult)
[![Status](https://img.shields.io/badge/Status-In_Progress-yellow.svg)](#)

---

## 📌 Project Overview
This repository hosts the end-to-end **Exploratory Data Analysis (EDA)** and **Supervised Machine Learning Classification** for the **UCI Adult (Census Income)** dataset.

The objective is to analyze socioeconomic, demographic, and occupational factors influencing income levels and build classification models to predict whether an individual's annual income exceeds **$50,000/year** (`<=50K` vs `>50K`).

### Dataset Summary
* **Source:** [UCI Machine Learning Repository — Adult Dataset](https://archive.ics.uci.edu/dataset/2/adult)
* **Records:** 48,842 instances
* **Attributes:** 14 features (6 numerical, 8 categorical)
* **Target:** `income` (`<=50K` or `>50K`)

---

## 👥 Team Members & Responsibilities

| Member | Assigned Stages | Focus Area |
| :--- | :--- | :--- |
| **Dhruven** | **Stage 1 & Stage 2A** | Data Understanding, Cleaning, Handling missing values (`" ?"`), Duplicate removal, Boundary validation, and **Univariate EDA**. |
| **Prit** | **Stage 2B** | Outlier analysis, Skewness treatment (Log transforms), Categorical Encoding (One-Hot & Label), and **Bivariate/Multivariate EDA**. |
| **Punit** | **Stage 3 & Stage 4** | Train-Test split (80/20 Stratified), Feature Scaling, Model Training (4+ Classifiers), Evaluation (F1, ROC-AUC), Feature Importance, and **Final Executive Report**. |

---

## 📁 Planned Project Structure

```text
census-income-eda-ml/
├── data/
│   ├── raw/                 # Original raw census data
│   └── processed/           # Cleaned and transformed datasets
├── notebooks/               # Individual member notebooks & master notebook
├── models/                  # Exported model files (.joblib / .pkl)
├── reports/                 # Exported visual figures, plots & report PDF
├── .gitignore               # Ignored cache, checkpoints & environments
├── README.md                # Project documentation
└── requirements.txt         # Project dependencies
```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/punit169/census-income-eda-ml.git
cd census-income-eda-ml
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 🗺️ Project Roadmap

- [x] **Stage 1: Problem Definition & Data Sourcing**
  - Acquired the UCI Adult Census Income dataset (48,842 instances, 14 features) and finalized the project scope.
- [ ] **Stage 2: Data Preprocessing & Exploratory Data Analysis**
  - Data cleaning (resolving `" ?"` missing values, duplicates, type conversions), outlier detection, skewness transformations, and univariate/bivariate visualizations.
- [ ] **Stage 3: Supervised Model Building & Evaluation**
  - Training and benchmarking four classification algorithms (Logistic Regression, Decision Tree, Random Forest, KNN) evaluated using F1-score, Confusion Matrices, and ROC-AUC curves.
- [ ] **Stage 4: Insights & Reporting**
  - Feature importance analysis to identify key income determinants, synthesis of findings, and final project documentation.
