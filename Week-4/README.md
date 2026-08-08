# Bank Loan Approval Prediction

## Project Objective

The objective of this project is to build a Machine Learning classification system that predicts whether a loan application is likely to be approved or rejected based on applicant information.

The project implements and compares two Machine Learning models:

- Random Forest
- XGBoost

The better-performing model is then used for loan approval prediction.

---

## Dataset

The project uses the provided bank loan dataset.

The dataset contains:

- 614 rows
- 13 columns

The target variable is:

`Loan_Status`

Where:

- `Y` = Loan Approved
- `N` = Loan Rejected

---

## Features Used

The following applicant information is used for prediction:

- Gender
- Married
- Dependents
- Education
- Self_Employed
- ApplicantIncome
- CoapplicantIncome
- LoanAmount
- Loan_Amount_Term
- Credit_History
- Property_Area

`Loan_ID` is removed because it is only an identifier.

---

## Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the provided CSV dataset.
2. Inspected the dataset structure and data types.
3. Checked for missing values.
4. Filled missing categorical values using the mode.
5. Filled missing numerical values using the median.
6. Removed `Loan_ID`.
7. Separated features and target variable.
8. Encoded the target variable:
   - Y → 1
   - N → 0
9. Encoded categorical features using one-hot encoding.
10. Split the dataset into training and testing sets.

The dataset was divided into:

- 80% training data
- 20% testing data

---

## Machine Learning Models

Two classification algorithms were trained:

### 1. Random Forest

Random Forest combines multiple decision trees and uses their predictions to make the final classification.

### 2. XGBoost

XGBoost is a gradient boosting algorithm that builds decision trees sequentially to improve prediction performance.

---

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Classification Report

### Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Random Forest | 83.74% | 84.95% | 92.94% | 88.76% |
| XGBoost | 77.24% | 83.53% | 83.53% | 83.53% |

---

## Best Performing Model

Based on the evaluation results, **Random Forest** performed better than XGBoost on the selected test set.

Random Forest achieved:

- Accuracy: 83.74%
- Precision: 84.95%
- Recall: 92.94%
- F1-Score: 88.76%

Therefore, Random Forest is used as the final prediction model.

---

## Loan Prediction

The prediction system accepts applicant information such as:

- Gender
- Married
- Dependents
- Education
- Self Employment
- Applicant Income
- Coapplicant Income
- Loan Amount
- Loan Amount Term
- Credit History
- Property Area

The trained Random Forest model then predicts:

`Loan Approved`

or

`Loan Rejected`

---

## Project Workflow

CSV Dataset

↓

Data Inspection

↓

Data Cleaning

↓

Categorical Encoding

↓

Train/Test Split

↓

Random Forest & XGBoost

↓

Model Evaluation

↓

Model Comparison

↓

Best Model Selection

↓

Loan Approval Prediction

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn

---

## How to Run

### 1. Clone or download the project

Place the provided dataset inside the `data` folder.

### 2. Install the required libraries

```bash
pip install -r requirements.txt
