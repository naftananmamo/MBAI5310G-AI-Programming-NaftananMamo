# Assignment 4 – Part 1: Supplier Delay Risk Prediction (ProcurePro Office)

## Overview

This project focuses on predicting supplier delivery risk for ProcurePro Office, a B2B company that distributes office supplies to medium-sized organizations. Supplier delays can negatively impact inventory availability, customer satisfaction, and operational efficiency. The goal of this project is to develop a machine learning model that can identify purchase orders that are at risk of being delayed before the promised delivery date.

## Business Problem

ProcurePro Office faces uncertainty in supplier deliveries. Late deliveries can disrupt operations and lead to customer dissatisfaction. By predicting supplier delay risk in advance, the company can proactively monitor high-risk orders, communicate with suppliers, and implement mitigation strategies.

## Dataset

The dataset contains information about purchase orders, suppliers, and operational factors that may influence delivery performance.

### Target Variable

- **Supplier_Delay_Risk** – Indicates whether a purchase order is considered high risk for delay.

### Input Features

Examples of features used for prediction include:

- Supplier_Region
- Contract_Type
- Shipping_Mode
- Payment_Terms
- Seasonal_Period
- Order_Value_CAD
- Number_of_Line_Items
- Promised_Lead_Time_Days
- Past_On_Time_Rate
- Supplier_Rating
- Urgent_Order
- Backorder_History
- Quality_Incidents_Last_6M
- Prior_Delays_Last_6M
- Distance_KM
- Inventory_Buffer_Days
- Seasonal_Demand_Index

## Data Preparation

The following preprocessing steps were performed:

1. Loaded and inspected the dataset.
2. Checked the dataset dimensions and data types.
3. Checked for missing values and duplicate records.
4. Filled missing values in the `Backorder_History` column using the mode.
5. Separated features (`X`) and target variable (`y`).
6. Identified categorical and numerical variables.
7. Applied One-Hot Encoding to categorical variables.
8. Split the dataset into training and testing sets.
9. Applied preprocessing using a ColumnTransformer.

## Machine Learning Model

A Decision Tree Classifier was trained to predict supplier delay risk.

### Model Configuration

- Algorithm: Decision Tree Classification
- Max Depth: 4
- Random State: 42

## Model Evaluation

The model was evaluated using the following performance metrics:

| Metric | Score |
|----------|----------|
| Accuracy | 77.78% |
| Precision | 77.27% |
| Recall | 85.00% |
| F1-Score | 80.95% |

### Confusion Matrix

| Actual / Predicted | No | Yes |
|-------------------|----|----|
| Actual No | 22 | 10 |
| Actual Yes | 6 | 34 |

Where:

- True Negative (TN): 22
- False Positive (FP): 10
- False Negative (FN): 6
- True Positive (TP): 34

## Classification Report

| Class | Precision | Recall | F1-Score | Support |
|---------|---------|---------|---------|---------|
| No | 0.79 | 0.69 | 0.73 | 32 |
| Yes | 0.77 | 0.85 | 0.81 | 40 |

Overall Accuracy: **0.78**

The model achieved stronger performance in identifying high-risk purchase orders (Yes class) than low-risk purchase orders (No class). The high recall score indicates that most high-risk orders were successfully detected.

## Overfitting Analysis

Two Decision Tree models were compared:

| Model | Training Accuracy | Testing Accuracy |
|---------|---------|---------|
| Controlled Decision Tree | 90.63% | 77.78% |
| Overfitted Decision Tree | 100.00% | 70.83% |

The overfitted Decision Tree achieved perfect training accuracy but performed worse on the testing data. This suggests that the model memorized the training dataset rather than learning patterns that generalize to unseen purchase orders.

The controlled Decision Tree provided better balance between training and testing performance and was therefore selected as the preferred model.

## Key Findings

- The model correctly classified approximately 78% of purchase orders.
- Recall was the strongest metric at 85%, meaning most high-risk orders were identified.
- Only 6 high-risk orders were missed by the model.
- The controlled Decision Tree generalized better than the overfitted model.
- The model can be used as an early warning system for supplier delivery delays.

## Business Impact

The model can help ProcurePro Office:

- Identify high-risk purchase orders before delays occur.
- Improve supplier monitoring and management.
- Reduce operational disruptions caused by late deliveries.
- Support inventory and logistics planning.
- Improve customer satisfaction through proactive intervention.

## Conclusion

The Decision Tree model demonstrated good performance in predicting supplier delay risk, achieving an accuracy of 77.78% and a recall of 85.00%. The results show that machine learning can effectively support procurement decision-making by identifying orders that may require additional attention before delivery deadlines are missed.
