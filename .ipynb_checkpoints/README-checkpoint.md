# Credit Risk Analysis Report
Using lending data, I built a machine-learning model that evaluated borrowers and identifies their credit-worthiness. 

## Overview of the Analysis
1. I used the 'lending_data.csv', containing: 
   - loan_size
   - interest_rate
   - borrower_income
   - debt_to_income
   - num_of_accounts
   - derogatory_marks
   - total_debt
   - loan_status
The loan_status column contains either 0 or 1, where 0 means that the loan is healthy, and 1 means that the loan is at a high risk of defaulting. I stored the data in a dataframe.

2. To assess creditworthiness, I initially stored the labels set from the 'loan_status' column in the variable 'y' and the features DataFrame (excluding 'loan_status') in the variable 'x'. 