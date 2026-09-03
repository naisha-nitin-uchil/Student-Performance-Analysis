
Today 9:12 PM
0d750529-2372-4b4a-ae88-4fab32602a81.png

30362a68-2153-45d7-ae69-981516b13bdb.png

bda0c439-b954-4682-8b02-eaab52aec03e.png

6939dcc4-10d5-4d7d-a02b-268b1164b54a.png

240e9363-8d81-4f6c-a485-0d57a66c2956.png

Ah yes — that means you accidentally created .gitignore inside the Python folder. No problem. 👍

We need it at the project root, at the same level as README.md, LICENSE, and requirements.txt.

It should look like this:

Student Performance Analysis/
│
├── .gitignore          ← HERE
├── .gitattributes
├── LICENSE
├── README.md
├── requirements.txt
│
├── Dataset/
├── Power Bi/
└── Python/
    └── student_analysis.ipynb
Do this in VS Code
Since .gitignore is currently inside Python:

In Explorer, find .gitignore under Python.

Right-click .gitignore → Cut.

Right-click the top-level Student Performance Analysis folder.

Select Paste.

Then open .gitignore and make sure it contains:

# VS Code
.vscode/

# Python
__pycache__/
*.py[cod]
*.pyo

# Jupyter
.ipynb_checkpoints/

# Virtual environments
venv/
.venv/
env/

# OS files
.DS_Store
Thumbs.db

# Python cache
*.pyc
Save it.

Then check your Explorer
You should see .gitignore above Dataset, Power Bi, and Python, like:

Student Performance Analysis
├── .gitignore
├── .gitattributes
├── LICENSE
├── README.md
├── requirements.txt
├── Dataset
├── Power Bi
└── Python
Don't run any Git commands yet. Once you've moved it, send me a screenshot and I'll guide you to the next step.


rs\uchil\OneDrive\Desktop\Projects\Student Performance Analysis> git add .gitignore
(base) PS C:\Users\uchil\OneDrive\Desktop\Projects\Student Performance Analysis> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitignore
        modified:   Dataset/StudentPerformanceFactors_Encoded.csv
        renamed:    Python/student_analysis.ipynb/student_analysis.ipynb -> Python/student_analysis.ipynb
        modified:   README.md
        modified:   requirements.txt

(base) PS C:\Users\uchil\OneDrive\Desktop\Projects\Student Performance Analysis> 

Perfect. ✅ This is exactly what we want.

Your .gitignore is now correctly staged at the project root, and .vscode/ is no longer appearing as an untracked file. Excellent.

Current staged changes
.gitignore                              ← new
Dataset/StudentPerformanceFactors_Encoded.csv
Python/student_analysis.ipynb           ← renamed/moved
README.md                                ← modified
requirements.txt                         ← modified
So the Git cleanup is essentially done.

🚫 Don't commit yet
Before we commit, I want to improve the actual project content. Otherwise we'd just be committing the current README and files and then immediately changing them again.

Next: Let's inspect your project
I want to look at your:

README.md

Python notebook

Power BI dashboard screenshot

requirements.txt

Then I'll tell you exactly what should be changed.

Since these are files in your current project, please upload these 4 files here:

README.md

Python/student_analysis.ipynb

Power Bi/dashboard.png

requirements.txt

You can select all four together when uploading.

Don't change anything else in Git yet. Once I have them, we'll build the README around your actual work and make the repository genuinely strong rather than just cosmetically organized.


dashboard.png

README.md
File

requirements.txt
Document

student_analysis(1).ipynb
File

Student Performance Analysis.pbix
File

Great — now that you've uploaded the actual README, notebook, requirements, and dashboard, I can give you a much more precise plan.

I reviewed the notebook in detail. Your project is actually stronger than the current GitHub README makes it look.

What you have
6,607 student records

20 variables

Data cleaning and missing-value handling

Exploratory data analysis

Correlation analysis

Categorical encoding

4 regression models

Model evaluation using MAE, RMSE and R²

Random Forest feature importance

Interactive Power BI dashboard

Your current README only says that it's an interactive Power BI dashboard, so it doesn't communicate most of this work. 


Your requirements.txt is also appropriate for the notebook because it includes Pandas, NumPy, Matplotlib, Seaborn and Scikit-learn. 


⭐ What I recommend changing
1. README — major upgrade
I've prepared a complete professional README based on your actual notebook and dashboard, not generic filler.

Download the improved README

It includes:

Project overview

Dashboard preview

Objectives

Dataset details

Tools

Workflow

Data cleaning

EDA

Actual model results

Feature importance

Power BI features

Repository structure

Installation instructions

Future improvements

2. Your dashboard is good
Your dashboard screenshot is actually quite presentable.

You have:

Total Students: 7K

Average Exam Score: 67.24

Average Attendance: 79.98

Average Study Hours: 19.98

Attendance vs Exam Score

Gender comparison

Motivation comparison

Parental education

School type

Teacher quality

Interactive filters

For GitHub, though, I'd eventually change 7K → 6,607 so the dashboard agrees exactly with the underlying dataset.

3. 🚨 Most important technical fix: your notebook paths
Currently your notebook contains paths like:

C:/Users/uchil/OneDrive/Desktop/Projects/Student Performance Analysis/Dataset/StudentPerformanceFactors.csv
That means another person cloning your GitHub repository cannot run the notebook without changing the path.

We should change it to something like:

df = pd.read_csv("../Dataset/StudentPerformanceFactors.csv")
That will make the project genuinely reproducible.

4. Your ML results are actually a strong addition
Your notebook tested:

Model	R²
Linear Regression	0.689
Decision Tree	0.230
Random Forest	0.655
Gradient Boosting	0.725
So instead of presenting this as only a Power BI project, we can present it as an:

End-to-end Data Analytics & Machine Learning project

That's considerably stronger for your portfolio.

5. Feature importance gives you a good story
Your Random Forest analysis found:

Attendance          38.0%
Hours Studied       24.2%
Previous Scores      9.2%
Tutoring Sessions    3.5%
Sleep Hours          3.0%
So your README can communicate that attendance and study hours were the most important predictive features in the Random Forest analysis.

That's much more meaningful than simply saying "student performance was analyzed."

One thing I want to fix before we commit
There is a small methodological issue in the notebook:

LabelEncoder()
is being applied to all categorical input variables.

For example, converting categories into 0, 1, 2 can imply an artificial numerical order to a model such as Linear Regression.

For a polished portfolio project, I'd prefer using One-Hot Encoding for nominal categorical features and a proper preprocessing pipeline.

We don't have to make that change immediately, though.

Our next sequence should be:
① Replace the README with the professional version

↓

② Fix the notebook's hard-coded paths

↓

③ Decide whether to improve the encoding

↓

④ Check the Power BI file/name

↓

⑤ Add the dashboard image to GitHub README

↓

⑥ Commit all changes

↓

⑦ Push to GitHub

↓

⑧ Final recruiter review

Let's do Step 1 now
Download:

README_professional.md

Then in VS Code:

Open your current README.md.

Select everything.

Replace it with the contents of the downloaded README_professional.md.

Save it.

Don't commit yet.

After you've replaced the README, tell me "done", and we'll fix the notebook paths next. 


README_professional.md
Document


Library
/
README_professional.md


Student Performance Analysis
An end-to-end student performance analysis project using Python, Pandas, Scikit-learn, and Power BI to explore the factors associated with students' exam performance.

📊 Dashboard Preview

The interactive Power BI dashboard summarizes student performance using key KPIs and comparisons across demographic, academic, and learning-related factors.

![Student Performance Dashboard](Power%20Bi/dashboard.png)

🎯 Project Objectives
Analyze the factors associated with student exam performance.

Explore relationships between attendance, study hours, previous scores, and exam scores.

Compare average exam performance across gender, motivation level, school type, parental education, and teacher quality.

Prepare the dataset for machine learning.

Build and compare regression models for exam-score prediction.

Identify the most important features contributing to model predictions.

📁 Dataset
The dataset contains 6,607 student records and 20 columns covering academic, demographic, behavioral, and learning-related factors.

Key variables include:

Hours Studied

Attendance

Previous Scores

Motivation Level

Sleep Hours

Tutoring Sessions

Family Income

Teacher Quality

School Type

Parental Education Level

Physical Activity

Gender

Exam Score

The raw dataset contains missing values in Teacher Quality, Parental Education Level, and Distance from Home. These were handled using the mode before further analysis.

🛠️ Tools & Technologies
Python

Pandas — data loading, cleaning, and analysis

NumPy — numerical operations

Matplotlib & Seaborn — data visualization

Scikit-learn — preprocessing, model training, and evaluation

Power BI — interactive dashboard and KPI reporting

Excel — data dictionary/reference

🔄 Project Workflow
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
🧹 Data Preparation
The Python analysis includes:

Dataset shape and column inspection

Missing-value analysis

Duplicate-record check

Removal of duplicate records

Missing-value treatment using the mode

Summary statistics

Numerical correlation analysis

Exploratory visualizations

Categorical feature encoding

Preparation of training and testing datasets

📈 Exploratory Data Analysis
The analysis explores:

Distribution of exam scores

Gender distribution

Motivation-level distribution

Family-income distribution

Average exam score by gender

Average exam score by motivation level

Average exam score by school type

Average exam score by teacher quality

Exam score vs. hours studied

Attendance vs. exam score

Exam-score distributions across categories

Correlation between numerical variables

Key EDA Findings
The dataset contains 6,607 students.

Average exam score is approximately 67.24.

Average attendance is approximately 79.98%.

Average study time is approximately 19.98 hours.

Attendance has a strong positive relationship with exam score in the correlation analysis.

Hours studied also shows a positive relationship with exam score.

🤖 Machine Learning
The target variable is:

Exam_Score
The remaining variables are used as input features.

The dataset is split into:

5,285 training records

1,322 testing records

The following regression models were compared:

Model	MAE	RMSE	R² Score
Linear Regression	1.016	2.097	0.689
Decision Tree	1.729	3.298	0.230
Random Forest	1.131	2.209	0.655
Gradient Boosting	0.825	1.970	0.725
Best Model
Gradient Boosting achieved the best R² score among the tested models:

MAE: 0.825

RMSE: 1.970

R²: 0.725

This means the Gradient Boosting model performed best among the four tested models on the selected test split.

🔎 Feature Importance
The Random Forest analysis identified the following features as the most important for prediction:

Attendance — 0.380

Hours Studied — 0.242

Previous Scores — 0.092

Tutoring Sessions — 0.035

Sleep Hours — 0.030

These values represent model feature importance and should be interpreted as predictive importance rather than proof of causal relationships.

📊 Power BI Dashboard
The dashboard provides interactive views of:

Total students

Average exam score

Average attendance

Average study hours

Exam score by gender

Average exam score by motivation level

Average exam score by parental education

Average exam score by school type

Average exam score by teacher quality

Attendance vs. exam score

Interactive filters are available for:

Gender

Parental Education

Motivation Level

School Type

📂 Repository Structure
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
▶️ How to Run the Python Analysis
1. Clone the repository
git clone https://github.com/naisha-nitin-uchil/Student-Performance-Analysis.git
cd Student-Performance-Analysis
2. Install dependencies
pip install -r requirements.txt
3. Open the notebook
Open:

Python/student_analysis.ipynb
Run the cells from top to bottom.

Note: The notebook should use relative dataset paths so that it can run on another computer without changing Windows-specific file locations.

💡 Future Improvements
Replace hard-coded local file paths with relative paths.

Use a reproducible preprocessing pipeline for machine learning.

Compare additional regression models and tune hyperparameters.

Add cross-validation for more robust model evaluation.

Add model-prediction visuals to the Power BI dashboard.

Improve dashboard accessibility and simplify visual styling.

👩‍💻 Author
Naisha Nitin Uchil

Computer Science Student
Interested in Data Analytics, Python, AI, and Business Intelligence.

