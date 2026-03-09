# Bank-Loan-Risk-Analysis


## Project Overview
This project analyzes bank loan approval data to identify the factors influencing loan approval decisions.

The analysis focuses on understanding how variables such as income, credit history, property area, and education impact the likelihood of loan approval.

The project was implemented using **Python for data analysis and visualization**.

---

## Tools & Technologies

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook
- Data Analysis

---

## Dataset

Dataset Source: Kaggle

Files Used:
- train.csv
- test.csv

The dataset includes the following attributes:

- Applicant Income
- Co-Applicant Income
- Loan Amount
- Loan Term
- Credit History
- Property Area
- Education
- Employment Status
- Loan Status

---

## Data Analysis Workflow

### 1 Data Loading
The dataset was loaded using **Pandas**.

```python
df = pd.read_csv("train.csv")
###2 Data Exploration

Initial exploration included:

Checking dataset structure

Identifying missing values

Understanding variable types

df.info()
df.isnull().sum()
3 Data Cleaning

Missing values were handled using:

Mode for categorical variables

Median for numerical variables

Example:

df['Gender'] = df['Gender'].fillna(df['Gender'].mode()[0])
df['LoanAmount'] = df['LoanAmount'].fillna(df['LoanAmount'].median())
4 Exploratory Data Analysis

EDA was performed to analyze relationships between variables.

Examples:

Loan approval by credit history

Loan approval by property area

Loan approval by education

Income vs loan amount analysis

Example analysis:

pd.crosstab(df['Credit_History'], df['Loan_Status'], normalize='index') * 100
Key Insights

Applicants with good credit history have significantly higher loan approval rates.

Semi-urban applicants show higher loan approval rates.

Higher income applicants tend to receive larger loan approvals.

Credit history is the strongest predictor of loan approval.

Business Value

This analysis helps financial institutions:

Understand loan approval patterns

Identify risk factors

Improve loan approval decision processes

Reduce default risk
