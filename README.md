# Customer-Transaction
Machine learning project for Customer Transaction using Logistic Regression, XGBoost and LightGBM, with a focus of handling class imbalance and optimizing classification performance.
💳 Customer Transaction Prediction

📌 Project Overview

This project focuses on predicting whether a customer will make a specific transaction based on their available customer-related features.

The project uses Machine Learning classification algorithms to identify customers who are likely to make a transaction.

A major challenge in this dataset is class imbalance, where the number of customers who did not make a transaction is much higher than the number of customers who did.

Different machine learning models were trained and evaluated to identify the best-performing model.

---

🎯 Objective

The main objective of this project is to:

- Predict whether a customer will make a transaction.
- Analyze patterns in customer data.
- Handle the highly imbalanced target variable.
- Compare different classification algorithms.
- Select the best-performing model based on appropriate evaluation metrics.

---

🗂️ Dataset

The dataset contains:

- 200,000 rows
- 202 columns
- 1 target variable
- 200 numerical predictor variables
- 1 ID column

Dataset Columns

The main columns include:

ID_code
target
var_0
var_1
var_2
...
var_199

Target Variable

The "target" variable represents whether a customer made a transaction.

Target| Meaning
0| Customer did not make a transaction
1| Customer made a transaction

The dataset is highly imbalanced, with significantly fewer positive transactions than negative transactions.

---

🔍 Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand the structure and characteristics of the dataset.

The analysis included:

- Dataset shape
- Data types
- Missing-value analysis
- Duplicate analysis
- Target distribution
- Numerical feature distributions
- Descriptive statistics
- Feature relationships
- Class imbalance analysis

The target distribution was examined using both counts and proportions.

---

⚠️ Class Imbalance

The dataset contains a highly imbalanced target variable.

Approximately:

Negative class (0): 143,922
Positive class (1): 16,078

Because of this imbalance, accuracy alone is not a suitable metric for evaluating the models.

Therefore, additional evaluation metrics were considered, including:

- ROC-AUC
- Precision
- Recall
- F1 Score

---

🛠️ Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset.
2. Examined data types and missing values.
3. Checked for duplicate records.
4. Separated the target variable from the input features.
5. Removed the ID column from the modeling features.
6. Performed a stratified train-test split.
7. Addressed the class imbalance during model training.

Stratification was used to maintain a similar proportion of positive and negative classes in the training and testing datasets.

---

🤖 Machine Learning Models

Three classification algorithms were evaluated:

1. Logistic Regression

Logistic Regression was used as a baseline classification model.

ROC-AUC: 0.8599
F1 Score: 0.375

---

2. XGBoost

XGBoost was used as a powerful tree-based classification algorithm.

ROC-AUC: 0.8829
F1 Score: 0.5297

---

3. LightGBM

LightGBM was evaluated as another gradient boosting algorithm and achieved the best overall performance.

The model was trained with class imbalance handling and threshold optimization.

ROC-AUC: 0.8898
F1 Score: 0.5462
Precision: 0.5032
Recall: 0.5973

---

📊 Model Comparison

Model| ROC-AUC| F1 Score
Logistic Regression| 0.8599| 0.3750
XGBoost| 0.8829| 0.5297
LightGBM| 0.8898| 0.5462

🏆 Final Model

Based on the evaluation results, LightGBM was selected as the final model because it achieved the highest ROC-AUC and F1 Score among the evaluated models.

The final classification threshold was optimized rather than relying only on the default threshold of 0.5.

---

📈 Evaluation Metrics

ROC-AUC

ROC-AUC measures how well the model can distinguish between customers who make a transaction and those who do not.

A higher ROC-AUC indicates better ranking/discrimination performance.

Precision

Precision measures how many of the customers predict
