# Module 12 Report Template

## Purpose of Analysis
The goal of this project was to develop a machine learning model capable of predicting the creditworthiness of loan applicants. The dataset, obtained from a peer-to-peer lending platform, includes historical lending data with borrower financial details and corresponding loan outcomes.

## Objective
- The primary task was to predict a binary target variable, loan_status, where:

    - 0 represents a healthy loan (low risk of default)

    - 1 represents a high-risk loan (likely to default)

- An initial review of the target variable using value_counts() revealed a strong class imbalance—healthy loans significantly outnumber high-risk ones. This imbalance presents a challenge for accurate prediction.

## Machine Learning Workflow

- Loaded and explored the dataset (lending_data.csv)

- Split the data into feature variables (X) and the target label (y)

- Divided the data into training and testing sets using train_test_split

- Trained a logistic regression model with LogisticRegression(random_state=1)

- Evaluated the model using:

    - Confusion matrix

    - Classification report (accuracy, precision, recall)

## Results: Logistic Regression Model

- **Accuracy**: ~94%

- **Precision** (Class 0 - Healthy Loans): ~0.94

- **Recall** (Class 0 - Healthy Loans): ~1.00

- **Precision** (Class 1 - High-Risk Loans): ~0.85

- **Recall** (Class 1 - High-Risk Loans): ~0.02

*Note: These values may vary slightly depending on system configuration and scikit-learn version.

## Summary
While the logistic regression model performed well overall—particularly in identifying healthy loans—it struggled significantly with detecting high-risk loans. The recall for class 1 (high-risk) was just 2%, likely due to the skewed class distribution.

### Recommendations for Improvement

- To address the class imbalance and improve performance on high-risk loans, consider:

- Applying resampling techniques such as:

- SMOTE (Synthetic Minority Over-sampling Technique)

- Random oversampling or undersampling

- Using class_weight='balanced' in the logistic regression model

- Trying more robust models like:
    - Random Forest
    - Gradient Boosting methods (e.g., XGBoost)
    - Incorporating feature engineering to enhance predictive power
