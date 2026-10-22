# 🎓 Engineering Graduate Campus Placement & Salary Prediction
### IT462: Exploratory Data Analysis — Course Project (DA-IICT / DAU)

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange.svg)](https://scikit-learn.org/)
[![Dataset](https://img.shields.io/badge/Dataset-AMEO_2015_(AMCAT)-brightgreen.svg)](https://www.kaggle.com/datasets/manishkc06/engineering-graduate-salary-prediction)
[![Syllabus](https://img.shields.io/badge/Curriculum-IT462_Syllabus_100%25_Covered-purple.svg)](#-it462-syllabus-coverage-matrix)

---

## 📌 Project Overview
This repository hosts the end-to-end **Exploratory Data Analysis (EDA)**, **Inferential Statistical Modeling**, and **Predictive Classification Pipeline** for the real-world **Aspiring Minds Employment Outcome (AMEO 2015)** dataset.

The project investigates the multi-dimensional determinants of employment outcomes for Indian engineering graduates, analyzing how academic track records (`collegeGPA`, 10th/12th percentages), standardized cognitive competencies (Logical, Quantitative, English), technical programming mastery, college institutional tiers, and personality traits impact placement success and compensation packages (`Salary`).

The entire analytical workflow is built strictly in accordance with the official **IT462 Exploratory Data Analysis Syllabus** (covering Classical Tukey EDA, Missingness Mechanisms, Descriptive Shape & Dispersion, Covariance & Correlation, Linear Data Fitting, Time Series Trends, and Advanced PCA / Automated Profiling).

---

## 📊 Dataset Specification (AMEO 2015: 2,998 Records, 34 Features)

* **Source:** Real-world National Employability Study by Aspiring Minds (AMCAT), hosted on [Kaggle](https://www.kaggle.com/datasets/manishkc06/engineering-graduate-salary-prediction).
* **Sample Size:** 2,998 actual engineering graduates across 1,173 colleges in 26 Indian states.
* **Feature Categories:**
  * **Academic Background:** `collegeGPA`, `10percentage`, `10board`, `12percentage`, `12board`, `Degree`, `Specialization`, `GraduationYear`.
  * **Institutional Context:** `CollegeTier` (Tier 1 vs Tier 2), `CollegeCityTier`, `CollegeState`.
  * **AMCAT Cognitive Competencies:** `English`, `Logical`, `Quant` (Standardized national percentiles).
  * **Technical & Domain Expertise:** `ComputerProgramming`, `Domain`, `ComputerScience`, `ElectronicsAndSemicon`, `MechanicalEngg`, `ElectricalEngg`, `CivilEngg`.
  * **Psychometric Personality Inventory (Five-Factor Model):** `conscientiousness`, `agreeableness`, `extraversion`, `nueroticism`, `openess_to_experience`.
  * **Placement Outcomes:** `Salary` (Continuous annual CTC in INR) and derived placement classification tiers (`placed_tier`).

---

## 📋 IT462 Syllabus Coverage Matrix (Modules 1 to 9)

Every single topic and keyword from Appendix - I of the official IT462 syllabus is directly addressed across the three project notebooks:

| Module # | Syllabus Module Title | Core Topics Prescribed in Syllabus | Assigned Member | Implementation Location |
| :--- | :--- | :--- | :--- | :--- |
| **Module 1** | **Data and Statistics** | What is Data?; Data Science Pipeline; Role of EDA in ML; Structured vs Unstructured Data; Population vs Sample | **Dhruven** & **Punit** | `01_dhruven_cleaning_univariate.ipynb` (Section 2) & `03_punit_model_building.ipynb` (Section 12) |
| **Module 2** | **Measurement Scales** | Nominal Scale, Ordinal Scale, Interval Scale, Ratio Scale; Discrete vs Continuous Variables | **Dhruven** | `01_dhruven_cleaning_univariate.ipynb` (Section 4) |
| **Module 3** | **Data Collection & Sampling** | Census vs Sample; Sampling Bias; Random Sampling (SRS); Stratified Sampling; Cluster Sampling; Design of Experiments | **Punit** | `03_punit_model_building.ipynb` (Section 3 & 8) |
| **Module 4** | **Data Import & Cleaning** | Import from sources; Data Inspection & Insights; Duplicate Detection; Inconsistent Formats; Invalid Entries (`-1` sentinel codes); Data Type Conversion; Encoding Issues; Transformations | **Dhruven** (Cleaning) & **Prit** (Encoding) | `01_dhruven_cleaning_univariate.ipynb` (Section 3 & 5) & `02_prit_transformation_bivariate.ipynb` (Section 8) |
| **Module 5** | **Missing Data Analysis** | Missingness Mechanisms (MCAR, MAR, MNAR); Missingness Visualization (`missingno` / heatmap); Missing Data Treatment | **Dhruven** | `01_dhruven_cleaning_univariate.ipynb` (Section 6) |
| **Module 6** | **Descriptive Summary** | Measures of Central Tendency (Mean, Median, Mode); Variation (Variance, Std Dev, IQR); Shape (Skewness, Kurtosis); MAD (Median Absolute Deviation); Coefficient of Variation (CV); Tukey's Five-Number Summary | **Dhruven** | `01_dhruven_cleaning_univariate.ipynb` (Section 7) |
| **Module 7** | **Univariate & Bivariate Analysis** | Numeric & Visualization methods: Histogram, Density Plot (KDE), Boxplot, Violin Plot, Bar Chart, Scatter Plot, Covariance Matrix, Correlation, Crosstabs with marginals, Heatmaps | **Dhruven** (Univariate) & **Prit** (Bivariate) | `01_dhruven_cleaning_univariate.ipynb` (Section 8) & `02_prit_transformation_bivariate.ipynb` (Section 3, 4, 5) |
| **Module 8** | **Correlation Analysis & Data Fitting** | Pearson Correlation; Spearman Rank Correlation; Correlation Matrix; Multicollinearity (VIF); Regression models (Simple & Multiple Linear Regression); Goodness of Fit ($R^2$, Adj $R^2$, RMSE, Residual vs Fitted, Q-Q Plot) | **Prit** | `02_prit_transformation_bivariate.ipynb` (Section 4, 6, 7) |
| **Module 9** | **Advanced EDA & Dashboards** | Principal Component Analysis (PCA: Scree Plot, 2D Biplot); Time Series EDA & Trend Detection (Graduation cohorts 2010–2015, Rolling 2-yr Averages, Academic Lag); Seasonality; Automated Profiling (Sweetviz, ydata-profiling, D-Tale); Plotly Interactive Dashboards; Data Storytelling; Tableau/PowerBI Export | **Punit** | `03_punit_model_building.ipynb` (Section 4, 5, 6, 7) |
| **Final Project** | **Applied Modeling & Synthesis** | Collect real empirical dataset; Address research difficulties; Benchmark 4 ML Models; ROC Curves; Confusion Matrices; Feature Importance; PO1–PO5 Outcomes Synthesis | **Punit (Lead)**, **Dhruven**, **Prit** | All Notebooks & `reports/` |

---

## 👥 Syllabus-Aligned Team Work Allocation

| Team Member | Assigned Stages | Syllabus Modules | Core Deliverables | Starter Notebook |
| :--- | :--- | :--- | :--- | :--- |
| **Dhruven** | **Stage 1 & 2A** | **Modules 1, 2, 4, 5, 6, 7** | Data foundations & taxonomy; Measurement scales classification; Data cleaning & sentinel value handling (`-1`); Missingness diagnostics (**MCAR, MAR, MNAR** with `missingno`); Comprehensive descriptive summaries (**Mean, Median, Mode, Variance, Std Dev, IQR, MAD, CV, Five-Number Summary, Skewness, Kurtosis**); Univariate distributions (**Histograms, KDE Density Plots, Boxplots, Violin Plots, Bar Charts**); Export `ameo_cleaned.csv`. | [`notebooks/01_dhruven_cleaning_univariate.ipynb`](notebooks/01_dhruven_cleaning_univariate.ipynb) |
| **Prit** | **Stage 2B** | **Modules 4, 7, 8** | Ingest `ameo_cleaned.csv`; Bivariate visualizations (**Scatter Plots, Grouped Box/Violin Plots**); Covariance Matrix (`df.cov()`); Correlation analysis (**Pearson vs Spearman comparison, Correlation Matrix & Heatmaps**); Contingency tables (**Crosstabs with marginals & heatmaps**); Multicollinearity diagnostics using **VIF (Variance Inflation Factor)**; Regression modeling (**Simple & Multiple Linear Regression for Salary, Goodness of Fit $R^2$, Adj $R^2$, RMSE, Residual Diagnostics**); Feature engineering & encoding; Export `ameo_encoded.csv`. | [`notebooks/02_prit_transformation_bivariate.ipynb`](notebooks/02_prit_transformation_bivariate.ipynb) |
| **Punit** | **Stage 3 & 4** | **Modules 1, 3, 9 & Final ML** | Ingest `ameo_encoded.csv`; Data collection & sampling analysis (**Census vs Sample, Sampling Bias, Empirical comparison of SRS vs Stratified vs Cluster Sampling, Design of Experiments**); **Time Series EDA & Cohort Trend Detection (2010–2015 cohorts, 2-year rolling moving averages, degree duration lag)**; **PCA Dimensionality Reduction (Scree Plot, 2D Biplot / Loadings)**; **Sweetviz Automated Profiling Report**; **Plotly Multi-Panel Interactive Dashboard**; **Tableau / PowerBI CSV Export**; Supervised classification benchmark (Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, ROC curves, Confusion Matrices, Gini Feature Importance); Executive Synthesis & PO alignment. | [`notebooks/03_punit_model_building.ipynb`](notebooks/03_punit_model_building.ipynb) |

---

## 📁 Repository Structure

```text
campus-placement-eda-ml/
├── data/
│   ├── raw/
│   │   └── Engineering_graduate_salary.csv  # Real-world AMEO benchmark (2,998 rows, 34 columns)
│   └── processed/                           # Cleaned and feature-engineered datasets
│       ├── ameo_cleaned.csv                 # Exported by Dhruven (Stage 1 & 2A)
│       ├── ameo_encoded.csv                 # Exported by Prit (Stage 2B)
│       └── ameo_tableau_ready.csv           # Exported by Punit (Stage 3 & 4)
├── notebooks/
│   ├── 01_dhruven_cleaning_univariate.ipynb     # Stage 1 & 2A (Dhruven)
│   ├── 02_prit_transformation_bivariate.ipynb   # Stage 2B (Prit)
│   └── 03_punit_model_building.ipynb            # Stage 3 & 4 (Punit)
├── models/                                  # Exported trained models (.joblib / .pkl)
├── reports/                                 # Visual figures, plots, HTML reports & dashboard
│   └── figures/
│       ├── sweetviz_placement_report.html       # Automated Sweetviz profiling
│       └── interactive_placement_dashboard.html # Interactive Plotly dashboard
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
print(f"Loaded: {df.shape[0]:,} rows x {df.shape[1]} columns")
```

### 3. Execution Sequence for Team
1. **Dhruven** opens `notebooks/01_dhruven_cleaning_univariate.ipynb`, completes Stages 1 & 2A, and exports `data/processed/ameo_cleaned.csv`.
2. **Prit** opens `notebooks/02_prit_transformation_bivariate.ipynb`, ingests `ameo_cleaned.csv`, completes Stage 2B, and exports `data/processed/ameo_encoded.csv`.
3. **Punit** opens `notebooks/03_punit_model_building.ipynb`, ingests `ameo_encoded.csv`, conducts Sampling Analysis, Time Series Cohort Trends, PCA, Sweetviz & Plotly dashboards, and executes the Supervised ML pipeline.
