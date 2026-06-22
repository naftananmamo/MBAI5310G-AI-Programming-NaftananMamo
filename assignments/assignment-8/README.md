# HomeIQ Customer Support Text Classification Using NLP

## Project Overview

This project applies Natural Language Processing (NLP) and machine learning techniques to automatically classify customer support messages into different support categories.

HomeIQ receives customer inquiries from multiple channels such as email, chat, phone transcripts, mobile applications, and product reviews. These messages contain valuable information about customer complaints, product issues, and feedback. However, manually reviewing and categorizing large volumes of customer messages can be time-consuming.

The goal of this project is to build a text classification model that can automatically predict the category of a customer support message.

The model helps improve customer service efficiency by:
- Automatically routing customer requests to the correct support team
- Reducing response time
- Identifying common customer issues
- Understanding customer feedback trends

---

# Business Problem

Customer support teams receive a large amount of unstructured text data every day. Important information about product issues and customer satisfaction is contained within these messages.

This project solves the problem of automatically identifying the type of customer issue based on the customer's written message.

The model predicts support categories such as:

- Voice Assistant
- Security Alert
- Warranty Return
- Installation
- Connectivity
- Energy Saving

This classification system can help HomeIQ improve customer support operations and make faster decisions based on customer feedback.

---

# Dataset Description

The dataset contains customer support records with the following information:

| Column | Description |
|--------|-------------|
| SupportID | Unique identifier for each support request |
| SupportDate | Date the support message was created |
| Channel | Communication method used by the customer |
| City | Customer location |
| DeviceType | HomeIQ device related to the issue |
| CustomerSegment | Customer type |
| SupportMessage | Customer text inquiry or feedback |
| SupportCategory | Target variable representing the issue category |
| IssueSeverity | Importance level of the issue |

---

# Project Workflow

The project follows a complete NLP machine learning pipeline:

## 1. Data Inspection

The dataset was loaded and analyzed by examining:

- Dataset shape
- Column information
- Missing values
- Target variable distribution

---

## 2. Text Preprocessing

The `SupportMessage` column was selected as the main text feature.

The following preprocessing steps were applied:

- Converted text to lowercase
- Removed punctuation
- Tokenized text
- Removed stopwords
- Applied lemmatization
