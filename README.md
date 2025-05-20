# credit-risk-classification


## Overview

This project applies supervised machine learning to assess the credit risk of borrowers using historical data from a peer-to-peer lending platform. A logistic regression model is developed to classify loans as either:

- `0`: Low-risk (healthy loan)
- `1`: High-risk (likely to default)

This analysis supports lenders in making informed credit decisions by identifying potential risk patterns.

---

## Machine Learning Workflow

1. Loaded and cleaned data from `lending_data.csv`
2. Separated features (`X`) from target labels (`y`)
3. Split the dataset into training and testing sets using `train_test_split`
4. Trained a logistic regression model with `scikit-learn`
5. Evaluated performance using a confusion matrix and classification report

---

## Model Performance

**Logistic Regression Results:**

- Accuracy: ~94%
- Precision (Low-risk loans): ~0.94  
- Recall (Low-risk loans): ~1.00  
- Precision (High-risk loans): ~0.85  
- Recall (High-risk loans): ~0.02  

*Note: The model struggles to detect high-risk loans due to significant class imbalance.*

---

## Analysis and Interpretation

The model effectively identifies low-risk loans but performs poorly on high-risk classifications. With recall for high-risk loans near zero, the model underperforms where accurate detection is most critical.

---

## Recommendations

To improve the model's predictive power for high-risk loans:

- Address class imbalance using techniques such as:
  - SMOTE (Synthetic Minority Over-sampling)
  - Adjusting class weights or applying undersampling
- Experiment with alternative algorithms:
  - Random Forest
  - Gradient Boosting (e.g., XGBoost)
- Enhance performance through feature engineering and normalization

---

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Jupyter Notebook
