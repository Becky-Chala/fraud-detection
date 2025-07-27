# Fraud Detection Project

## Overview
This project focuses on building machine learning models to detect fraudulent transactions using two datasets:

1. **Credit Card Transactions**
2. **Online Fraud Data (with geolocation and user behavior features)**

The core goal is to compare the performance of a simple model (Logistic Regression) and a powerful ensemble model (Random Forest) using metrics appropriate for **imbalanced classification problems**.

---

## Problem Statement
Fraudulent transactions are rare but critical events that require precise detection techniques. Traditional accuracy metrics often fail in imbalanced datasets, hence our approach emphasizes:

- **F1-Score**
- **AUC-PR (Area Under Precision-Recall Curve)**
- **Confusion Matrix**

---

## Project Structure
```
fraud-detection/
│
├── data/
│   ├── raw/                  # Original datasets (Fraud_Data.csv, IpAddress_to_Country.csv, creditcard.csv)
│
├── notebooks/
│   └── task1.ipynb          # Data preprocessing, EDA, feature engineering
│   └── task2.ipynb          # Model training and evaluation
│
├── .gitignore               # Excludes .venv and data folders from Git
├── README.md                # Project overview and instructions
└── requirements.txt         # Python dependencies
```

---

## Tasks Completed

### Task 1: Data Preprocessing & Feature Engineering
- Handled missing values
- Converted timestamps
- Mapped IPs to countries using interval indexing
- Engineered features like:
  - `hour_of_day`, `day_of_week`, `time_since_signup`
  - `user_tx_count`, `device_tx_count`
- Encoded categorical features
- Applied **SMOTE** to balance classes
- Scaled numeric features using **StandardScaler**

### Task 2: Model Building and Evaluation
Models built and compared:
- **Logistic Regression** (baseline)
- **Random Forest Classifier** (ensemble)

Evaluation Metrics used:
- **F1 Score**
- **AUC-PR**
- **Confusion Matrix**
- **Classification Report**

Both models were tested on the scaled and resampled fraud dataset.

---

## Key Insights
- **Random Forest outperformed Logistic Regression** significantly in terms of F1 and AUC-PR, demonstrating better handling of nonlinear patterns in the data.
- Ensemble methods are more robust for fraud detection when trained on resampled and well-engineered features.

---

## Setup Instructions
1. Clone the repository:
```bash
git clone https://github.com/Becky-Chala/fraud-detection.git
```
2. Navigate to the project:
```bash
cd fraud-detection
```
3. Create and activate a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # For Windows: .venv\Scripts\activate
```
4. Install dependencies:
```bash
pip install -r requirements.txt
```
