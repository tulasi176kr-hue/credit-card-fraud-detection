# credit-card-fraud-detection
Credit Card Fraud Detection is a machine learning project developed using Python and Scikit-learn to detect potentially fraudulent credit card transactions.The project uses transaction details suchas amount,merchant risk,transaction time,distance from home,and transaction type to classify transaction as normal /fraudulent using Logistic Regression.
# Credit Card Fraud Detection Using Machine Learning

## Project Overview

Credit Card Fraud Detection is a machine learning project developed using Python to identify potentially fraudulent credit card transactions.

The project analyzes transaction characteristics such as transaction amount, transaction time, distance from home, merchant risk score, number of transactions, card presence, international transactions, and online transactions. A Logistic Regression model is used to classify transactions as either normal or fraudulent.

The project is created for educational and academic purposes.

## Objectives

* Analyze credit card transaction data.
* Explore normal and fraudulent transactions.
* Identify important transaction features.
* Preprocess the transaction dataset.
* Train a machine learning classification model.
* Predict potentially fraudulent transactions.
* Evaluate the performance of the model.
* Visualize transaction and fraud patterns.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

## Machine Learning Algorithm

### Logistic Regression

The project uses Logistic Regression for binary classification.

The model classifies each transaction into one of two categories:

* 0 = Normal Transaction
* 1 = Fraudulent Transaction

Logistic Regression is suitable for binary classification problems where the output belongs to one of two classes.

## Dataset

The project uses the following dataset:

`credit_card_transactions.csv`

The dataset contains transaction-related information used to train and test the machine learning model.

### Dataset Features

| Feature               | Description                                                 |
| --------------------- | ----------------------------------------------------------- |
| transaction_id        | Unique identification number of the transaction             |
| amount                | Transaction amount                                          |
| hour                  | Hour at which the transaction occurred                      |
| distance_from_home_km | Distance of the transaction from the cardholder's home      |
| merchant_risk_score   | Risk score associated with the merchant                     |
| transactions_last_24h | Number of transactions made in the previous 24 hours        |
| card_present          | Indicates whether the physical card was present             |
| international         | Indicates whether the transaction was international         |
| online_transaction    | Indicates whether the transaction was made online           |
| fraud                 | Target variable indicating normal or fraudulent transaction |

## Project Workflow

The project follows these steps:

1. Load the transaction dataset.
2. Display the first few records.
3. Check the dataset size.
4. Check for missing values.
5. Handle missing numerical values.
6. Analyze normal and fraudulent transaction distribution.
7. Separate features and target variable.
8. Split the dataset into training and testing data.
9. Standardize numerical features.
10. Train the Logistic Regression model.
11. Predict transaction classes.
12. Calculate fraud probabilities.
13. Evaluate the model.
14. Analyze important transaction features.
15. Generate visualizations.

## Data Preprocessing

Missing numerical values are handled using median values.

The `transaction_id` column is removed because it is only an identifier and does not provide useful information for prediction.

The remaining features are used as input variables.

The numerical features are standardized using `StandardScaler`.

## Train-Test Split

The dataset is divided into:

* 80% Training Data
* 20% Testing Data

The training data is used to train the machine learning model, while the testing data is used to evaluate its performance.

Stratified splitting is used to maintain the proportion of normal and fraudulent transactions in both datasets.

## Class Balancing

Fraud detection datasets can contain significantly fewer fraudulent transactions than normal transactions.

To address this issue, the Logistic Regression model uses:

`class_weight="balanced"`

This gives greater importance to the minority class during model training.

## Model Evaluation

The model is evaluated using:

### Accuracy

Accuracy represents the percentage of correctly classified transactions.

### Precision

Precision measures how many transactions predicted as fraudulent are actually fraudulent.

### Recall

Recall measures how many actual fraudulent transactions are correctly identified by the model.

Precision and recall are particularly important for fraud detection because accuracy alone may not provide a complete picture of model performance.

### Classification Report

The classification report provides precision, recall, F1-score, and support for both normal and fraudulent transactions.

### Confusion Matrix

The confusion matrix shows the number of correctly and incorrectly classified transactions for each class.

## New Transaction Prediction

The project demonstrates how the trained model can be used to predict a new transaction.

The example transaction contains information such as:

* Transaction amount
* Transaction hour
* Distance from home
* Merchant risk score
* Number of transactions in the last 24 hours
* Card presence
* International transaction status
* Online transaction status

The model provides:

* Predicted transaction class
* Fraud probability

## Feature Analysis

The project examines Logistic Regression coefficients to identify transaction features that have greater influence on the model's predictions.

The features are ranked based on the absolute value of their coefficients.

This helps understand which transaction characteristics are more influential in the classification process.

## Data Visualization

The project generates two visualizations.

### 1. Fraud Transaction Analysis

This visualization shows the relationship between transaction amount and merchant risk score and distinguishes between normal and fraudulent transactions.

Output file:

`fraud_transaction_analysis.png`

### 2. Fraud Class Distribution

This visualization displays the number of normal and fraudulent transactions in the dataset.

Output file:

`fraud_class_distribution.png`

## Project Structure

```text
Credit_Card_Fraud_Detection/
│
├── credit_card_fraud_detection.py
├── credit_card_transactions.csv
├── requirements.txt
├── README.md
│
├── fraud_transaction_analysis.png
└── fraud_class_distribution.png
```

## Installation

Make sure Python is installed on your computer.

Install the required libraries using:

```bash
pip install -r requirements.txt
```

The main libraries used are:

```text
pandas
numpy
matplotlib
scikit-learn
```

## How to Run

Open the project folder in Command Prompt or Terminal.

Run:

```bash
python credit_card_fraud_detection.py
```

The program will:

* Load the transaction dataset.
* Check and clean missing values.
* Display transaction class distribution.
* Train the Logistic Regression model.
* Predict test transactions.
* Calculate accuracy, precision, and recall.
* Display the classification report and confusion matrix.
* Predict a new transaction.
* Calculate fraud probability.
* Display important transaction features.
* Generate visualization graphs.

## Applications

Credit card fraud detection techniques can be useful for:

* Online payment security
* Banking systems
* E-commerce transactions
* Financial institutions
* Transaction monitoring
* Risk management
* Suspicious transaction detection

## Limitations

* The dataset included with this project is synthetic.
* The project is intended for educational purposes.
* Real-world fraud detection requires much larger and more complex datasets.
* Fraud patterns can change over time.
* A production fraud detection system would require additional security, monitoring, and validation techniques.

## Future Enhancements

The project can be improved by:

* Using real-world transaction datasets.
* Comparing multiple classification algorithms.
* Implementing Random Forest and Gradient Boosting.
* Using advanced anomaly detection techniques.
* Developing a real-time fraud detection system.
* Creating a web-based prediction interface.
* Adding an interactive dashboard.
* Improving fraud probability calibration.
* Deploying the model as an application.

## Project Information

**Project Name:** Credit Card Fraud Detection

**Domain:** Machine Learning and Financial Security

**Programming Language:** Python

**Machine Learning Type:** Supervised Learning

**Problem Type:** Binary Classification

**Algorithm:** Logistic Regression

**Target Variable:** Fraud

## Dataset Note

The transaction dataset included in this project is synthetic and created for educational and classroom machine-learning practice. It does not contain real credit card information.

## Important Note

This project is intended for educational purposes and should not be used as a production fraud-detection system without additional testing, validation, security controls, and real-world data.
