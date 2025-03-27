# Credit-Card-Fraud-Detection

# Situation (S)

Credit card fraud is a major issue, leading to financial losses for banks and customers. Fraudulent transactions are rare but can cause significant damage. The challenge lies in detecting these fraudulent transactions effectively from a highly imbalanced dataset, where genuine transactions vastly outnumber fraudulent ones.
This project aims to build a machine learning model to detect fraudulent transactions using an anomaly detection approach. The dataset used contains transaction details and a fraud label.

# Task (T)

The objective of the project is to:

* Analyze the dataset and understand fraud distribution.
* Preprocess data to handle missing values, imbalanced classes, and normalization.
* Implement anomaly detection models such as:
     * Isolation Forest
     * Local Outlier Factor (LOF)
     * One-Class SVM
* Evaluate model performance using accuracy, classification reports, and visualization techniques.

# Action (A)

The following actions were taken to complete the task:

1. Data Loading & Exploration

The dataset (creditcard.csv) was loaded using pandas.
It was checked for missing values (data.isnull().values.any()).
The class distribution was analyzed to confirm the dataset was highly imbalanced, with fraud cases forming a small percentage.

2. Data Preprocessing
   
Feature Scaling: Since transaction amounts vary significantly, normalization was applied.
Class Balancing: Standard techniques like undersampling or oversampling might be needed, but in this case, anomaly detection models inherently handle imbalance.

3. Model Selection & Training

* Isolation Forest
A tree-based anomaly detection technique that isolates outliers.
It assigns an anomaly score to transactions and classifies them accordingly.

* Local Outlier Factor (LOF)
A density-based approach that compares local density around each point.
Fraudulent transactions are expected to have lower density compared to normal transactions.

* One-Class SVM

A support vector machine (SVM)-based approach that learns the boundary of normal transactions.
Any deviation from this boundary is classified as fraudulent.

4. Model Evaluation

* Performance Metrics:
accuracy_score, classification_report from sklearn.metrics were used.
The effectiveness of models was analyzed through precision, recall, and F1-score.

# Result (R)

* The Isolation Forest model performed well, detecting fraudulent transactions with a good balance of precision and recall.
* Local Outlier Factor (LOF) was also effective but slightly less reliable.
* One-Class SVM struggled due to the high-dimensional feature space.
* Fraud detection models showed promising results but need further optimization using hyperparameter tuning and feature engineering for real-world deployment.

To run this project, download the jupyter notebook file(.ipynb) and run the code. 

