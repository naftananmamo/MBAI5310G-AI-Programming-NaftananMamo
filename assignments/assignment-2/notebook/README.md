# Assignment 2 – Employee Attrition Prediction

## Overview
This assignment focuses on building a Logistic Regression machine learning model to predict employee attrition. The project includes data preprocessing, exploratory data analysis, model training, and performance evaluation using classification metrics.

The main goal is to analyze employee-related features and determine whether an employee is likely to leave the company.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## Folder Structure

```bash
assignment-2/
│
├── notebook/
│   ├── .ipynb_checkpoints/
│   ├── Assignment2.ipynb
│   ├── README.md
│   └── employee_attrition_prediction.csv
```

---

## Dataset

The dataset contains employee-related information such as:
- Age
- Salary
- Department
- Job Satisfaction
- Years at Company
- Work-Life Balance
- Attrition Status

---

## Project Workflow

### 1. Data Preprocessing
- Removed unnecessary columns
- Checked missing values
- Encoded categorical variables
- Split data into training and testing sets

### 2. Exploratory Data Analysis
- Visualized feature distributions
- Analyzed employee attrition patterns
- Identified important features

### 3. Model Building
The machine learning model used:
- Logistic Regression

### 4. Model Evaluation
The model was evaluated using:
- Accuracy
- Precision
- Recall
- F1-score

---

## Results Obtained

### Logistic Regression Model

| Metric | Score |
|------|------|
| Accuracy | 93.06% |
| Precision | 66.67% |
| Recall | 33.33% |
| F1-score | 44.44% |

---

## How to Run the Project

### Clone the Repository

```bash
git clone <repository-link>
```

### Navigate to the Folder

```bash
cd assignment-2/notebook
```

### Install Required Libraries

```bash
pip install pandas numpy matplotlib scikit-learn
```

### Run the Notebook

```bash
jupyter notebook
```

Open:

```bash
Assignment2.ipynb
```

---

## Key Learnings

- Data preprocessing techniques
- Classification model implementation
- Model evaluation metrics
- Understanding Logistic Regression
- Understanding model limitations

---

## Future Improvements

- Hyperparameter tuning
- Feature engineering
- Handling class imbalance
- Trying advanced machine learning models


