## Employee Attrition Prediction Using Machine Learning
## Project Overview
Built a machine learning model to predict employee attrition using HR analytics data
**Objective**: identify employees at risk of leaving and support data-driven retention strategies
## Dataset
Multiple datasets merged using EmployeeID
1) general_data.csv: employee demographics, role, income, experience
2) employee_survey_data.csv: job satisfaction, environment satisfaction, work-life balance
3) manager_survey_data.csv: manager performance ratings
4) in_time.csv / out_time.csv: daily login and logout timestamps
5) data_dictionary.xlsx: feature descriptions

## Data Preprocessing & Feature Engineering
Cleaned attendance data and removed holiday and redundant columns
Converted timestamps to datetime and computed average daily working hours (mean_time)
Handled missing values using logical imputation
Removed constant features (Over18, EmployeeCount, StandardHours)
One-hot encoded categorical variables and binary encoded Attrition

## Exploratory Data Analysis
Analyzed relationships between attrition and satisfaction, working hours, and experience
Performed correlation analysis to detect and remove highly correlated features

## Class Imbalance Handling
Applied SMOTE to balance the attrition classes before model training

## Feature Selection
Used ExtraTreesRegressor to identify key predictors
Important features included income, job level, age, working hours, and satisfaction scores

## Model Building & Evaluation
Train-test split: 80% training, 20% testing
**Models used:**
1)Logistic Regression
2)Decision Tree
3)Random Forest
4)SVM
5)KNN
6)XGBoost
**Evaluation metric: accuracy score**
**Best performance achieved by ensemble models (Random Forest, XGBoost)**

## Key Insights
Extreme working hours increase attrition risk
Low job and environment satisfaction strongly correlate with attrition
Certain departments and job roles show higher turnover

## Technologies Used
Python, Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn, Imbalanced-learn (SMOTE)
XGBoost

## Conclusion
Employee attrition can be effectively predicted using HR analytics and machine learning
The model provides actionable insights for proactive employee retention
Attrition is predictable, not random

## How to Run the Repository

1) Clone the repository:             git clone https://github.com/your-username/Employee-Attrition-Problem.git
                                     cd Employee-Attrition-Problem
2) Install required dependencies:    pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost

3)Ensure all dataset files (.csv and .xlsx) are in the project directory

4) Open the Jupyter Notebook        jupyter notebook

5) Run the notebook HR_analytics (Employee Attrition Prediction).ipynb 
