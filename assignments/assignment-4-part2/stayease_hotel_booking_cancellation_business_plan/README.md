# Assignment 4 – Part 2: Hotel Booking Cancellation Prediction

## Overview

This project focuses on predicting whether a hotel booking will be cancelled before the guest's arrival date. Booking cancellations can lead to revenue loss, inefficient room allocation, and operational challenges for hotels. The goal of this project is to develop a machine learning model that can identify bookings that are likely to be cancelled, allowing hotel management to take proactive measures.

## Business Problem

Hotels frequently experience booking cancellations, which can make occupancy planning difficult and reduce revenue. By predicting cancellations in advance, hotel managers can optimize room allocation, adjust pricing strategies, and implement overbooking policies more effectively.

## Dataset

The dataset contains information about hotel bookings, customer characteristics, reservation details, and booking history.

### Target Variable

- **Booking_Cancelled** – Indicates whether a booking was cancelled (1) or not cancelled (0).

### Input Features

Examples of features used for prediction include:

- Hotel_Type
- Arrival_Month
- Booking_Channel
- Market_Segment
- Customer_Type
- Reserved_Room_Type
- Meal_Plan
- Deposit_Type
- Lead_Time_Days
- Weekend_Nights
- Weekday_Nights
- Adults
- Children
- Previous_Cancellations
- Repeated_Guest
- Special_Requests
- Average_Daily_Rate
- Parking_Requested
- Loyalty_Points

## Data Preparation

The following preprocessing steps were performed:

1. Loaded and inspected the dataset.
2. Checked the dataset dimensions and data types.
3. Checked for missing values and duplicate records.
4. Separated features (`X`) and target variable (`y`).
5. Identified categorical and numerical variables.
6. Applied One-Hot Encoding to categorical variables.
7. Split the dataset into training and testing sets.
8. Applied preprocessing using a ColumnTransformer.

## Machine Learning Model

A Decision Tree Classifier was trained to predict booking cancellations.

### Model Configuration

- Algorithm: Decision Tree Classification
- Controlled Tree Depth
- Random State: 42

## Model Evaluation

The model was evaluated using the following performance metrics:

| Metric | Score |
|----------|----------|
| Accuracy | 55.26% |
| Precision | 31.71% |
| Recall | 68.42% |
| F1-Score | 43.33% |

### Confusion Matrix

| Actual / Predicted | No Cancellation | Cancellation |
|-------------------|----------------|-------------|
| Actual No Cancellation | 29 | 28 |
| Actual Cancellation | 6 | 13 |

Where:

- True Negative (TN): 29
- False Positive (FP): 28
- False Negative (FN): 6
- True Positive (TP): 13

## Classification Report

| Class | Precision | Recall | F1-Score | Support |
|---------|---------|---------|---------|---------|
| 0 (Not Cancelled) | 0.83 | 0.51 | 0.63 | 57 |
| 1 (Cancelled) | 0.32 | 0.68 | 0.43 | 19 |

Overall Accuracy: **0.55**

The model performed better at identifying bookings that were not cancelled than predicting cancellations. However, the model achieved a relatively strong recall for cancelled bookings, meaning it was able to identify most cancellations.

## Overfitting Analysis

Two Decision Tree models were compared:

| Model | Training Accuracy | Testing Accuracy |
|---------|---------|---------|
| Controlled Decision Tree | 76.97% | 55.26% |
| Overfitted Decision Tree | 100.00% | 57.89% |

The overfitted Decision Tree achieved perfect accuracy on the training dataset but did not significantly improve performance on the testing dataset. This indicates that the model memorized training examples rather than learning patterns that generalize effectively to unseen bookings.

The controlled Decision Tree provided a more balanced and interpretable model.

## Key Findings

- The model correctly classified 55.26% of bookings.
- The recall score of 68.42% indicates that the model successfully identified most cancelled bookings.
- The model generated a relatively high number of false positives, resulting in a lower precision score.
- The overfitted Decision Tree did not provide meaningful improvements on the testing data.
- Hotel booking cancellation appears to be a more challenging prediction problem than supplier delay prediction.

## Business Impact

The model can help hotel management:

- Identify bookings that are likely to be cancelled.
- Improve room allocation and occupancy planning.
- Support overbooking strategies.
- Reduce revenue loss associated with last-minute cancellations.
- Improve forecasting and operational decision-making.

## Conclusion

The Decision Tree model demonstrated moderate success in predicting hotel booking cancellations. While the model achieved a recall of 68.42%, its overall accuracy and precision were relatively low. The results suggest that the model can provide useful decision-support information, but additional feature engineering, hyperparameter tuning, or more advanced machine learning models may be needed to improve prediction performance.
