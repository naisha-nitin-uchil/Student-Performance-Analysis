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
