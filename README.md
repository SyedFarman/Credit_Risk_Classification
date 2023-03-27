# Credit_Risk_Classification

## Overview of the Analysis

The purpose of the analysis is to predict whether a loan is healthy or high-risk based on various financial data. The financial data includes loan size, interest rate, borrower income, and debt to income. The analysis involves building machine learning models and comparing their performance to choose the best one for the task.

The data contains 77,536 observations with 8 columns, including a target column called loan_status. The loan_status column has two classes: 0 for healthy loans and 1 for high-risk loans. The value counts for the target variable are 0: 75036 and 1: 2500.

The stages of the machine learning process are as follows:

1.	Data pre-processing and cleaning.
2.	Splitting the data into training and testing sets.
3.	Building and training a Logistic Regression model on the original imbalanced data.
4.	Building and training a Logistic Regression model on the oversampled data.
5.	Evaluating the models' performance and comparing their results.

Logistic Regression models are used in this analysis, and oversampling using the RandomOverSampler 
technique is applied to balance the target classes.

## Results
### •	Machine Learning Model 1: Logistic Regression on Original Data
        -	Balanced Accuracy Score: 0.952
        
      	-       Precision and Recall Scores:
        -	Healthy Loans (0): precision = 1.00, recall = 0.99, f1-score = 1.00
        -	High-Risk Loans (1): precision = 0.85, recall = 0.91, f1-score = 0.88

### •	Machine Learning Model 2: Logistic Regression on Oversampled Data
        -	Balanced Accuracy Score: 0.993
        
        Precision and Recall Scores:
        -	Healthy Loans (0): precision = 1.00, recall = 0.99, f1-score = 1.00
        -	High-Risk Loans (1): precision = 0.84, recall = 0.99, f1-score = 0.91

## Summary

The logistic regression model on the oversampled data performed better than the logistic regression model on the original data. This is evident from the higher balanced accuracy score of 0.993 for the oversampled data model compared to the balanced accuracy score of 0.952 for the original data model.

For the high-risk loans (1) label, the oversampled data model has a higher recall score of 0.99 compared to the original data model's recall score of 0.91, which means the oversampled data model correctly identifies more high-risk loans. However, the precision score for the high-risk loans label in the oversampled data model is slightly lower at 0.84 compared to the original data model's precision score of 0.85. This means that the oversampled data model has a slightly higher chance of misclassifying some healthy loans as high-risk loans.

Overall, both models performed well in predicting high-risk loans, but the logistic regression model on the oversampled data performed better due to its higher recall score. Therefore, we recommend using the logistic regression model on the oversampled data for predicting high-risk loans. 

However, the choice of model may depend on the specific problem and business requirements of the user, and it is essential to consider the consequences of making errors in the prediction of both healthy and high-risk loans.


