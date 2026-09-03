# 📊 Student Performance Analysis

An end-to-end data analytics and machine learning project that analyzes the factors associated with student exam performance using Python, Scikit-learn, and Power BI.

---

## 📌 Project Overview

This project analyzes student performance data to understand the factors associated with exam scores.

The project includes data cleaning, exploratory data analysis, categorical feature encoding, machine learning model training, model evaluation, feature importance analysis, and an interactive Power BI dashboard.

### 🎯 Objectives

- Analyze factors associated with student exam performance
- Clean and prepare the dataset
- Explore patterns and relationships in the data
- Analyze relationships between attendance, study hours, previous scores, and exam scores
- Encode categorical variables for machine learning
- Train and compare multiple regression models
- Evaluate model performance using MAE, RMSE, and R²
- Identify important features contributing to exam score predictions
- Build an interactive Power BI dashboard

---

## 📊 Dashboard Preview

The interactive Power BI dashboard summarizes student performance using key KPIs and comparisons across demographic, academic, and learning-related factors.

![Student Performance Dashboard](Power%20Bi/dashboard.png)

---

## 📁 Dataset

The dataset contains **6,607 student records and 20 variables** covering academic, demographic, behavioral, and learning-related factors.

### Key Variables

- Hours Studied
- Attendance
- Previous Scores
- Motivation Level
- Sleep Hours
- Tutoring Sessions
- Family Income
- Teacher Quality
- School Type
- Parental Education Level
- Physical Activity
- Gender
- Exam Score

The raw dataset contains missing values in **Teacher Quality**, **Parental Education Level**, and **Distance from Home**. These were handled using the mode before further analysis.

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas** — data loading, cleaning, and analysis
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Seaborn** — statistical visualization
- **Scikit-learn** — preprocessing, model training, and evaluation
- **Power BI** — interactive dashboard and KPI reporting
- **Excel** — data dictionary/reference

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Data Exploration
     ↓
Data Cleaning
     ↓
Exploratory Data Analysis
     ↓
Categorical Encoding
     ↓
Train/Test Split
     ↓
Regression Model Training
     ↓
Model Evaluation
     ↓
Feature Importance Analysis
     ↓
Power BI Dashboard

## Data Preparation

The Python analysis includes:

- Dataset shape and column inspection
- Missing-value analysis
- Duplicate-record check
- Removal of duplicate records
- Missing-value treatment using the mode
- Summary statistics
- Numerical correlation analysis
- Exploratory visualizations
- Categorical feature encoding
- Preparation of training and testing datasets

---

## 📈 Exploratory Data Analysis

The analysis explores:

- Distribution of exam scores
- Gender distribution
- Motivation-level distribution
- Family-income distribution
- Average exam score by gender
- Average exam score by motivation level
- Average exam score by school type
- Average exam score by teacher quality
- Exam score vs. hours studied
- Attendance vs. exam score
- Exam-score distributions across categories
- Correlation between numerical variables

### 🔎 Key EDA Findings

- The dataset contains **6,607 students**
- Average exam score is approximately **67.24**
- Average attendance is approximately **79.98%**
- Average study time is approximately **19.98 hours**
- Attendance shows a strong positive relationship with exam score in the correlation analysis
- Hours studied also shows a positive relationship with exam score

---

## 🤖 Machine Learning

The target variable is:

`Exam_Score`

The remaining variables are used as input features.

### Train-Test Split

The dataset is divided into:

- **5,285 training records**
- **1,322 testing records**

The split uses an **80/20 ratio** with a fixed random state for reproducibility.

### Models Used

The following regression models were trained and compared:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor
4. Gradient Boosting Regressor

---

## 📊 Model Performance

The models were evaluated using:

- **MAE** — Mean Absolute Error
- **RMSE** — Root Mean Squared Error
- **R² Score** — coefficient of determination

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 1.016 | 2.097 | 0.689 |
| Decision Tree | 1.729 | 3.298 | 0.230 |
| Random Forest | 1.131 | 2.209 | 0.655 |
| **Gradient Boosting** | **0.825** | **1.970** | **0.725** |

### 🏆 Best Model

**Gradient Boosting Regressor** achieved the best overall performance among the four tested models.

- **MAE:** 0.825
- **RMSE:** 1.970
- **R²:** 0.725

The model achieved the highest R² score and the lowest MAE and RMSE on the selected test split.

---

## 🔎 Feature Importance

Feature importance was analyzed using the **Random Forest** model to identify which factors contributed most to exam score predictions.

### Top Important Features

| Feature | Importance |
|---|---:|
| Attendance | 0.380 |
| Hours Studied | 0.242 |
| Previous Scores | 0.092 |
| Tutoring Sessions | 0.035 |
| Sleep Hours | 0.030 |

These values represent **predictive importance**, not proof of causal relationships.

---

## 📊 Power BI Dashboard

The Power BI dashboard provides interactive views of student performance through KPIs and visual comparisons.

### Dashboard Includes

- Total Students
- Average Exam Score
- Average Attendance
- Average Study Hours
- Exam Score by Gender
- Average Exam Score by Motivation Level
- Average Exam Score by Parental Education
- Average Exam Score by School Type
- Average Exam Score by Teacher Quality
- Attendance vs. Exam Score

### Interactive Filters

- Gender
- Parental Education
- Motivation Level
- School Type

---

## 📂 Repository Structure

```text
Student-Performance-Analysis/
│
├── Dataset/
│   ├── Data Dictionary.xlsx
│   ├── StudentPerformanceFactors.csv
│   ├── StudentPerformanceFactors_Cleaned.csv
│   └── StudentPerformanceFactors_Encoded.csv
│
├── Power Bi/
│   ├── dashboard.png
│   └── Student Performance Analysis.pbix
│
├── Python/
│   └── student_analysis.ipynb
│
├── .gitignore
├── .gitattributes
├── LICENSE
├── README.md
└── requirements.txt
