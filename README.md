Credit Card Fraud Detection Project
Overview
This project aims to identify fraudulent credit card transactions using machine learning techniques and statistical analysis. By preprocessing the data, balancing the dataset, and applying a logistic regression model, we achieved an accuracy of approximately 95%, demonstrating the effectiveness of the model in detecting fraudulent activities.

Objectives
Understand the Dataset:

Explore the structure and content of the data using functions like head(), tail(), and info().
Check for and handle missing values to ensure data quality.
Analyze Legitimate and Fraudulent Transactions:

Separate the data into two subsets: legitimate (Class = 0) and fraudulent (Class = 1).
Compute statistical measures for both subsets and compare their distributions.
Data Balancing (Undersampling):

Create a balanced dataset by undersampling legitimate transactions to match the count of fraudulent transactions.
Combine the undersampled legitimate transactions with fraudulent transactions to ensure a uniform distribution.
Build and Train the Model:

Split the balanced dataset into features and target variables.
Train a logistic regression model and evaluate its performance.
Evaluate Model Performance:

Assess the model using accuracy metrics for both training and testing datasets.
Verify the consistency of accuracy across datasets to ensure a good balance between bias and variance.
Tools and Libraries Used
NumPy: For numerical computations and handling arrays.
Pandas: For data manipulation, analysis, and preprocessing.
Scikit-learn:
train_test_split: To split the data into training and testing sets.
LogisticRegression: For training the classification model.
accuracy_score: To evaluate the model's performance.
Dataset
The dataset contains credit card transaction details, where:

Class = 0: Legitimate transaction
Class = 1: Fraudulent transaction
Dataset Features:
Numerical Features: Attributes like transaction amount, anonymized details (e.g., PCA components).
Target Variable (Class):
0: Legitimate transactions
1: Fraudulent transactions
Dataset Source:
The dataset is publicly available, such as the Kaggle Credit Card Fraud Detection Dataset.

Methodology
Data Exploration:

Basic Inspection:
Used head(), tail(), and info() to examine the structure and content of the dataset.
Missing Values:
Checked for null or missing values in the dataset.
Data Segmentation:

Split the dataset into two subsets:
Legitimate Transactions (Class = 0)
Fraudulent Transactions (Class = 1)
Statistical Analysis:

Calculated statistical measures (e.g., mean, median) for both legitimate and fraudulent transactions.
Compared the distributions of features for the two transaction types using:
python
Copy code
df.groupby("Class").mean()
Balancing the Dataset (Undersampling):

Sampled an equal number of legitimate transactions as fraudulent transactions:
python
Copy code
legit_sample = legit.sample(n=492)
Combined the sampled legitimate transactions with all fraudulent transactions to create a balanced dataset:
python
Copy code
balanced_data = pd.concat([legit_sample, fraud])
Feature and Target Separation:

Divided the balanced dataset into features (X) and target (y).
Model Training and Testing:

Split the data into training and testing subsets using train_test_split.
Trained a logistic regression model on the training dataset.
Predicted outcomes and calculated accuracy for both training and testing datasets.
Evaluation:

Observed an accuracy of approximately 95% for both training and testing datasets.
The similarity between training and testing accuracies indicates a well-balanced model with minimal bias and variance.



