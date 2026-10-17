# 🎓 Student Campus Placement Prediction & Package Analytics
### IT462 Machine Learning Course Project

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)](https://scikit-learn.org/)
[![Records](https://img.shields.io/badge/Records-100%2C000_Students-brightgreen.svg)](#)
[![Status](https://img.shields.io/badge/Status-In_Progress-yellow.svg)](#)

---

## 📌 Project Overview
This repository contains an end-to-end **Exploratory Data Analysis (EDA)** and **Supervised Machine Learning System** designed to predict **Student Campus Placement Outcomes** and analyze determinants of job offers and compensation packages.

Due to strict student data privacy regulations (DPDP Act / FERPA) prohibiting public sharing of private academic records, this project uses a large-scale, statistically modeled institutional benchmark of **100,000 university students** across 8 engineering and technical disciplines.

### Key Objectives
1. **Classification:** Predict whether a student gets placed (`placement_status`: 0 = Unplaced, 1 = Placed).
2. **Feature Impact Analysis:** Quantify the relative importance of academic standing (`cpi`), problem-solving ability (`coding_score`, `dsa_problems_solved`), project portfolio (`projects_count`), and prior industry experience (`internships`, `experience_months`).
3. **Package Distribution:** Model the salary expectations (`salary_lpa`) for placed graduates.

---

## 📊 Dataset Schema (100,000 Records, 18 Features)

| Feature | Type | Range / Values | Description |
| :--- | :--- | :--- | :--- |
| `student_id` | String | `STU_000001` - `STU_100000` | Unique student identifier |
| `branch` | Categorical | CSE, ICT, IT, ECE, MnC, EE, Mechanical, Civil | Engineering / Technology discipline |
| `cpi` | Numerical | 4.50 – 10.00 | Cumulative Performance Index |
| `attendance_rate` | Numerical | 60.0% – 100.0% | Overall classroom attendance percentage |
| `backlogs` | Numerical | 0 – 4 | Active / cleared backlog courses |
| `coding_score` | Numerical | 1.0 – 10.0 | Overall programming proficiency rating |
| `dsa_score` | Numerical | 1.0 – 10.0 | Data Structures & Algorithms rating |
| `dsa_problems_solved` | Numerical | 0 – 800+ | Total DSA / LeetCode problems solved |
| `projects_count` | Numerical | 0 – 6 | Number of completed projects |
| `has_major_project` | Binary | 0 or 1 | Completed a Capstone / Full-Stack / ML project |
| `internships` | Numerical | 0 – 3 | Number of corporate internships completed |
| `experience_months` | Numerical | 0 – 18 | Total cumulative internship/work experience in months |
| `aptitude_score` | Numerical | 25.0 – 100.0 | Standardized company aptitude test score |
| `communication_skills` | Numerical | 2.0 – 10.0 | Interviewer communication rating |
| `hackathons_attended` | Numerical | 0 – 5 | Hackathons / competitive technical events |
| `certifications_count` | Numerical | 0 – 5 | Professional online certifications completed |
| **`placement_status`** | Binary Target | 0 (Unplaced) / 1 (Placed) | **Primary classification target (~64.5% placed)** |
| **`salary_lpa`** | Numerical Target | 3.50 – 48.00 LPA | Annual CTC package in Lakhs Per Annum (NaN for unplaced) |

---

## 👥 Team Work Allocation & Responsibilities

| Team Member | Assigned Stages | Focus Areas & Deliverables | Notebook |
| :--- | :--- | :--- | :--- |
| **Dhruven** | **Stage 1 & 2A** | Data inspection, null value handling (`salary_lpa` unplaced logic), boundary validation, and **Univariate Distributions** (CPI, Coding, Projects, Experience, Backlogs). | `notebooks/01_dhruven_cleaning_univariate.ipynb` |
| **Prit** | **Stage 2B** | Outlier analysis, skewness treatment, feature engineering (`tech_readiness_score`, `experience_weight`), correlation heatmaps, and **Bivariate / Multivariate EDA** (CPI vs Placement, Coding vs Salary). | `notebooks/02_prit_transformation_bivariate.ipynb` |
| **Punit** | **Stage 3 & 4** | Stratified Train-Test split (80/20), Feature scaling, Model training (Logistic Regression, Decision Trees, Random Forest, Gradient Boosting), Hyperparameter tuning, ROC-AUC/F1 evaluation, Feature Importance, and **Executive Report**. | `notebooks/03_punit_model_building.ipynb` |

---

## 📁 Repository Structure

```text
census-income-eda-ml/
├── data/
│   ├── raw/
│   │   └── student_placement_data.csv       # 100,000-row benchmark dataset
│   └── processed/                           # Cleaned and feature-engineered datasets
├── notebooks/
│   ├── 01_dhruven_cleaning_univariate.ipynb     # Stage 1 & 2A (Dhruven)
│   ├── 02_prit_transformation_bivariate.ipynb   # Stage 2B (Prit)
│   └── 03_punit_model_building.ipynb            # Stage 3 & 4 (Punit)
├── scripts/
│   └── generate_placement_data.py           # Reproducible data generation script
├── models/                                  # Exported trained models (.joblib / .pkl)
├── reports/                                 # Visual figures, plots, and final report PDF
├── .gitignore
├── README.md
└── requirements.txt
```

---

## 🚀 Quickstart

### 1. Clone & Set Up
```bash
git clone https://github.com/punit169/census-income-eda-ml.git
cd census-income-eda-ml
pip install -r requirements.txt
```

### 2. Verify Dataset
```bash
python scripts/generate_placement_data.py
```
*(The raw dataset is already pre-generated and stored in `data/raw/student_placement_data.csv`)*
