Task 4: Loan Default Risk Prediction with Business Cost Optimization
## Introduction

Financial institutions face significant risk when approving loans. Approving a loan for a customer who later defaults can cause heavy financial loss, while rejecting a safe customer may lead to missed business opportunities. Traditional accuracy-based models are often insufficient for such scenarios.

This task focuses on building a loan default prediction system that not only predicts default risk but also optimizes decisions based on real business costs.

# Objectives

The main objectives of this task are:

To build a binary classification model to predict loan default risk

To handle missing values and categorical features appropriately

To use probability-based predictions instead of fixed thresholds

To optimize the classification threshold based on business cost considerations

To reduce costly false negatives (approving risky customers)

📊 Dataset Description

Dataset: Home Credit Default Risk Dataset (Kaggle)

Each row represents a loan applicant

Target variable:

TARGET = 1 → Client defaulted on loan

TARGET = 0 → Client did not default

Dataset contains numerical and categorical features with missing values

# Data Preprocessing

Loaded the training dataset (application_train.csv)

Removed the target variable from feature set

Handled missing values:

Numerical features → filled with median

Categorical features → filled with mode

Applied one-hot encoding to categorical variables

# Model Used
Logistic Regression

Used as a baseline classification model

Outputs probabilities instead of direct class labels

Well-suited for risk modeling and interpretability

# Business Cost Optimization

Instead of using the default threshold (0.5), a custom decision threshold was optimized using business costs:

False Positive (FP): Rejecting a good customer (low cost)

False Negative (FN): Approving a risky customer (high cost)

A range of thresholds was evaluated, and total business cost was calculated for each. The threshold with minimum cost was selected as optimal.

# Evaluation Metrics

Confusion Matrix

Precision, Recall, F1-score

Business Cost Curve

Evaluation focused on reducing financial loss, not just improving accuracy.

# Key Outcome

Optimized threshold significantly reduced false negatives

Business-aware decision-making outperformed default threshold approach

Demonstrated real-world banking risk modeling

# Libraries Used

pandas

numpy

scikit-learn

matplotlib

# Conclusion

This task demonstrates how machine learning models can be aligned with business objectives. By optimizing classification thresholds based on cost, the model provides more practical and financially sound decisions than traditional accuracy-based approaches.