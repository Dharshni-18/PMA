# Cyber Threat Analysis and Prediction using IBM SPSS Modeler

This project implements a three-level approach for cyber threat detection and prediction using IBM SPSS Modeler. It leverages both supervised and unsupervised machine learning techniques to classify network traffic as benign or malicious and to uncover hidden threat patterns in the data.

## 📊 Project Overview

The SPSS stream is divided into three analytical levels:

### 🔹 Level 1 – Baseline Classification
A basic C&R Tree model is used to establish an initial benchmark for predicting `threat_label`. This level focuses on generating interpretable decision rules and understanding influential variables in a straightforward classification setup.

### 🔹 Level 2 – Multi-Model Supervised Learning
This level integrates multiple supervised learning models including:
- C&R Tree
- Logistic Regression
- Auto Classifier (evaluates models like Random Forest and Neural Network internally)

All models are connected to a unified Evaluation node to assess performance using metrics such as accuracy, ROC, and precision. This helps in selecting the best model for deployment.

### 🔹 Level 3 – Unsupervised Threat Discovery
Unsupervised techniques such as:
- K-Means Clustering
- Anomaly Detection

are used to uncover patterns and anomalies that may not have been captured through labeled data. These outputs are cross-referenced with known threat labels to support threat intelligence.

## 📂 Files Included

- `cyber_threat_sample.csv`: Sample dataset used for training and testing models.
- `.str`: IBM SPSS Modeler stream file (can be opened directly in SPSS Modeler).
- `README.md`: This file.

## 🚀 How to Use

1. Open IBM SPSS Modeler.
2. Load the `.str` stream file.
3. Ensure `cyber_threat_sample.csv` is in your working directory.
4. Run each level step by step or all at once to generate model predictions and evaluations.
5. Use Graphboard and Analysis nodes to explore results visually.

## 📌 Evaluation & Deployment

- Evaluation nodes provide ROC, confusion matrix, and precision scores for all models.
- Best-performing supervised models are ready for export using PMML.
- Anomaly and clustering outputs offer additional insights for real-time threat monitoring and can be reviewed by analysts.


