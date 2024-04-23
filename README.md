# Credit Risk Analysis Report
Using lending data, I built a machine-learning model that evaluated borrowers and identifies their credit-worthiness. 

## Overview of the Analysis
1. I used the `lending_data.csv`, containing: 
   - loan_size
   - interest_rate
   - borrower_income
   - debt_to_income
   - num_of_accounts
   - derogatory_marks
   - total_debt
   - loan_status

The loan_status column contains either 0 or 1, where 0 means that the loan is healthy, and 1 means that the loan is at a high risk of defaulting. 

2. To assess creditworthiness, I initially stored the labels set from the `loan_status` column in the variable `y` and the features DataFrame (excluding `loan_status`) in the variable `x`.

3. Using the `train_test_split` module, I assigned a `random_state` of 1 to the function to make sure the train test split is consistent.

4. Using `LogisticRegression()` with a `random_state` of 1, the model was fit with the training data and predicted on testing data labels with `predict()` using the testing feature data, `X_test`, and the fitted model, `lr_model`

5. Based on `y_test` and `testing_prediction`, I generated a confusion matrix for the model with `confusion_matrix()`

6. I printed a classification report for the model with `classification_report()` udinh `y_test` and `testing_prediction`

## Results
- The precision and recall score for the healthy loans is 100%
- The accuracy of the model for predicting healthy loans is 100%
- The precision score for the high-risk loans is 85%
- The recall score for the high-risk loans is 91%
- The accuracy of the model for predicting high-risk loans is 88%
- The overall accuracy of the model is 99%

## Summary
The logistic regression model demonstrates high accuracy, achieving a perfect 100% prediction rate for healthy loans and an 88% accuracy rate for identifying high-risk loans. I suggest utilizing this model for smaller debts due to its ability to accurately predict loan health. However, I advise against solely depending on this model for predicting the likelihood of default for loans with larger total debts, as it is less precise in identifying high-risk loans in such cases. 