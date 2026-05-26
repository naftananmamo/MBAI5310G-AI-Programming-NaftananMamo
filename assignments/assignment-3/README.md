# Assignment 3 – Comparing Logistic Regression and SVM for Employee Attrition Prediction

## Overview
This assignment focuses on comparing a basic machine learning model, Logistic Regression, with a more advanced model, Support Vector Machine (SVM), for predicting employee attrition.

The project includes:
- Data preprocessing
- Exploratory data analysis
- Model training
- Performance evaluation
- Comparison of machine learning models

The goal is to determine which model performs better for employee attrition prediction.

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
assignment-3/
│
├── .ipynb_checkpoints/
│
├── Assignment3.ipynb
├── README.md
└── employee_attrition_prediction.csv
```

---

## Dataset

The dataset contains employee-related information used to predict attrition, including:
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
- Checked for missing values
- Removed unnecessary columns
- Encoded categorical variables
- Split data into training and testing sets

### 2. Exploratory Data Analysis
- Analyzed employee attrition patterns
- Visualized important features
- Identified relationships between variables

### 3. Model Training

The following models were implemented:

#### Basic Model
- Logistic Regression

#### Comparison Model
- Support Vector Machine (SVM)

### 4. Model Evaluation

The models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score

---

## Results Obtained

| Model | Accuracy | Precision | Recall | F1 Score |
|------|------|------|------|------|
| Logistic Regression | 0.9306 | 0.6667 | 0.3333 | 0.4444 |
| SVM | 0.9444 | 0.7500 | 0.5000 | 0.6000 |

---

## Model Comparison

- Logistic Regression was used as the baseline machine learning model.
- SVM achieved better performance across all evaluation metrics.
- SVM produced higher recall and F1-score, making it more effective for predicting employee attrition.
- The comparison demonstrated how advanced models can improve prediction performance over baseline models.

---

## How to Run the Project

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
Assignment3.ipynb
```

---

## Key Learnings

- Understanding baseline machine learning models
- Comparing machine learning algorithms
- Evaluating classification performance
- Understanding strengths and weaknesses of Logistic Regression and SVM
- Importance of preprocessing in machine learning

---

## Future Improvements

- Hyperparameter tuning
- Cross-validation
- Feature engineering
- Handling class imbalance
- Testing ensemble learning models



