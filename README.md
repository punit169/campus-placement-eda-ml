# 🎓 Engineering Graduate Campus Placement & Salary Prediction
### IT462: Exploratory Data Analysis — Course Project

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)](https://scikit-learn.org/)
[![Dataset](https://img.shields.io/badge/Dataset-AMEO_2015_(AMCAT)-brightgreen.svg)](https://www.kaggle.com/datasets/manishkc06/engineering-graduate-salary-prediction)
[![Syllabus](https://img.shields.io/badge/Curriculum-IT462_Syllabus_Aligned-purple.svg)](#)

---

## 📌 Project Overview
This repository hosts the end-to-end **Exploratory Data Analysis (EDA)**, **Inferential Statistical Modeling**, and **Predictive Classification Pipeline** for the real-world **Aspiring Minds Employment Outcome (AMEO 2015)** dataset.

The project investigates the multi-dimensional determinants of employment outcomes for Indian engineering graduates, analyzing how academic track records (`collegeGPA`, 10th/12th percentages), standardized cognitive competencies (Logical, Quantitative, English), technical programming mastery, college institutional tiers, and personality traits impact placement success and compensation packages (`Salary`).

The entire analytical workflow is built strictly in accordance with the **IT462 Exploratory Data Analysis Syllabus** (covering Classical Tukey EDA, Missingness Mechanisms, Descriptive Shape & Dispersion, Correlation & Multicollinearity, Linear Data Fitting, and Advanced PCA / Automated Profiling).

---

## 📊 Dataset Specification (AMEO 2015: 2,998 Records, 34 Features)

* **Source:** Real-world National Employability Study by Aspiring Minds (AMCAT), hosted on [Kaggle](https://www.kaggle.com/datasets/manishkc06/engineering-graduate-salary-prediction).
* **Sample Size:** 2,998 actual engineering graduates across India.
* **Feature Categories:**
  * **Academic Background:** `collegeGPA`, `10percentage`, `10board`, `12percentage`, `12board`, `Degree`, `Specialization`, `GraduationYear`.
  * **Institutional Context:** `CollegeTier` (Tier 1 vs Tier 2), `CollegeCityTier`, `CollegeState`.
  * **AMCAT Cognitive Competencies:** `English`, `Logical`, `Quant` (Standardized national percentiles).
  * **Technical & Domain Expertise:** `ComputerProgramming`, `Domain`, `ComputerScience`, `ElectronicsAndSemicon`, `MechanicalEngg`, `ElectricalEngg`, `CivilEngg`.
  * **Psychometric Personality Inventory (Five-Factor Model):** `conscientiousness`, `agreeableness`, `extraversion`, `nueroticism`, `openess_to_experience`.
  * **Placement Outcomes:** `Salary` (Continuous annual CTC in INR) and derived placement classification tiers.

---

## 👥 Syllabus-Aligned Team Work Allocation

| Team Member | Assigned Stages | Syllabus Modules Covered | Focus Areas & Deliverables | Starter Notebook |
| :--- | :--- | :--- | :--- | :--- |
| **Dhruven** | **Stage 1 & 2A** | **Modules 2, 4, 5, 6, 7** | Measurement scales classification (Nominal, Ordinal, Interval, Ratio); Missingness diagnostics (**MCAR, MAR, MNAR** with `missingno`); Data cleaning & invalid code handling (`-1` domain scores); Descriptive summaries (**Mean, Median, Mode, Variance, Std Dev, IQR, MAD, Coefficient of Variation, Tukey's Five-Number Summary, Skewness, Kurtosis**); Univariate distributions (**Histograms, KDE Density Plots, Boxplots, Violin Plots, Bar Charts**). | [`notebooks/01_dhruven_cleaning_univariate.ipynb`](notebooks/01_dhruven_cleaning_univariate.ipynb) |
| **Prit** | **Stage 2B** | **Modules 7 & 8** | Bivariate & multivariate analysis (**Scatter Plots, Covariance, Grouped Violin Plots, Crosstabs with marginals, Heatmaps**); Correlation analysis (**Pearson vs Spearman comparison, Correlation Matrix**); Multicollinearity diagnostics using **VIF (Variance Inflation Factor)**; Data fitting & Regression modeling (**Simple & Multiple Linear Regression for Salary, Goodness of Fit $R^2$, Adjusted $R^2$, Residual diagnostics**). | [`notebooks/02_prit_transformation_bivariate.ipynb`](notebooks/02_prit_transformation_bivariate.ipynb) |
| **Punit** | **Stage 3 & 4** | **Modules 1, 3, 9** | Sampling design (**Stratified 80/20 train-test split**); Advanced EDA via **PCA (Principal Component Analysis)** on cognitive/domain scores (**Scree plot, Explained Variance Ratio, 2D Biplot**); Automated EDA profiling report using **Sweetviz / ydata-profiling**; Interactive data storytelling using **Plotly Dashboards**; Supervised placement classification benchmark and **Executive Synthesis Report**. | [`notebooks/03_punit_model_building.ipynb`](notebooks/03_punit_model_building.ipynb) |

---

## 📁 Repository Structure

```text
campus-placement-eda-ml/
├── data/
│   ├── raw/
│   │   └── Engineering_graduate_salary.csv  # Real-world AMEO benchmark (2,998 rows, 34 columns)
│   └── processed/                           # Cleaned and feature-engineered datasets
├── notebooks/
│   ├── 01_dhruven_cleaning_univariate.ipynb     # Stage 1 & 2A (Dhruven)
│   ├── 02_prit_transformation_bivariate.ipynb   # Stage 2B (Prit)
│   └── 03_punit_model_building.ipynb            # Stage 3 & 4 (Punit)
├── models/                                  # Exported trained models (.joblib / .pkl)
├── reports/                                 # Visual figures, plots, Sweetviz HTML report & final report PDF
│   └── figures/
├── .gitignore
├── README.md
└── requirements.txt
```

---

## 🚀 Quickstart

### 1. Clone & Set Up Environment
```bash
git clone https://github.com/punit169/campus-placement-eda-ml.git
cd campus-placement-eda-ml
pip install -r requirements.txt
```

### 2. Verify Dataset Ingestion
```python
import pandas as pd
df = pd.read_csv('data/raw/Engineering_graduate_salary.csv')
print(f"Loaded: {df.shape[0]} rows x {df.shape[1]} columns")
```
