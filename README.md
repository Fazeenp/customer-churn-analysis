# Telco Customer Churn Analysis

This project focuses on analyzing and predicting customer churn using a real-world telecom dataset. The goal is to extract meaningful business insights and build robust machine learning models that accurately identify customers who are likely to leave the service.

---

## Project Structure

| File Name                        | Description                             |
|----------------------------------|-----------------------------------------|
| `Churn_Analysis_EDA.ipynb`      | Exploratory Data Analysis of the dataset |
| `Churn_Analysis_Model_Building.ipynb` | Model training, evaluation, and handling class imbalance |

---

## Dataset Information

- **Dataset Name:** Telco Customer Churn
- **Source:** Sample Telco dataset (commonly used for classification tasks)
- **File Format:** CSV
- **Total Records:** ~7,043
- **Features:** 21 columns including categorical, numerical, and the target column `Churn`

### Key Columns:
- `gender`, `SeniorCitizen`, `Partner`, `Dependents`
- `tenure`, `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, etc.
- `MonthlyCharges`, `TotalCharges`
- `Churn` (Target Variable)

---

## 1. Exploratory Data Analysis (`Churn_Analysis_EDA.ipynb`)

### Steps Performed:
- Loaded and inspected the dataset
- Checked for missing values and data types
- Analyzed feature distributions and outliers
- Visualized the target variable (`Churn`) distribution
- Derived key business insights based on patterns observed

### Observations:
- **Data Imbalance:** 73% Non-Churned vs. 27% Churned customers
- **Tenure Distribution:** 75% customers have tenure < 55 months
- **Churn Trends:**
  - Customers with **month-to-month** contracts are more likely to churn
  - Higher **monthly charges** and **fiber optic internet** usage are linked with churn
  - **Senior citizens** and **customers without partners** churn more

---

## 2. Model Building & Evaluation (`Churn_Analysis_Model_Building.ipynb`)

### Models Used:
- **Decision Tree Classifier**
- **Random Forest Classifier**

### Handling Imbalanced Dataset:
- Used **SMOTEENN** (SMOTE + Edited Nearest Neighbors) to oversample minority class and clean ambiguous samples

### Evaluation Metrics:
- **Precision**, **Recall**, and **F1-Score** were emphasized over Accuracy due to class imbalance
- Performance metrics were specifically monitored for **Class 1: Churned Customers**

### Results:
- **Random Forest** outperformed Decision Tree in overall accuracy and minority class recall
- Post-SMOTEENN application:
  - Improved F1-Score and recall for churn prediction
  - Achieved accuracy of ~92% with better balance across both classes

---

## Technologies Used

| Category       | Tools & Libraries                        |
|----------------|-------------------------------------------|
| Programming    | Python                                    |
| Data Analysis  | Pandas, NumPy                             |
| Visualization  | Matplotlib, Seaborn                       |
| ML Models      | Scikit-learn                              |
| Resampling     | imbalanced-learn (SMOTEENN)               |
| Environment    | Jupyter Notebook                          |

---

## Business Use Case

This project helps telecom businesses:
- Identify customers who are likely to churn
- Develop retention strategies based on churn drivers
- Make data-driven decisions to reduce customer attrition

---




