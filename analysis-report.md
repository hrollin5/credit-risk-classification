# Module 20 Report- Credit Risk Classification

## Overview of the Analysis

The objective of this analysis was to predict whether a loan will be healthy or high-risk.

The data provided included the following variables:

  * loan_size: The size of the loan.
  * interest_rate: The interest rate on the loan.
  * borrower_income: Income of the borrower.
  * debt_to_income: Debt-to-income ratio of the borrower.
  * num_of_accounts: Number of accounts the borrower has.
  * derogatory_marks: Number of derogatory marks on the borrower's credit report.
  * total_debt: Total debt of the borrower.
  
We utilized the Logistic Regression method for our analysis.
  
The dataset was imbalanced, with a larger number of healthy loans compared to high-risk ones. To address this, two machine learning models were developed using different sampling techniques: random sampling and random oversampling.


## Results

* Machine Learning Model 1 (Random Sampling):
  * Balanced Accuracy Score: 95.2%
  * Precision: Healthy Loan - 100%, Unhealthy Loan - 85%
  * Recall: Healthy Loan - 99%, Unhealthy Loan - 91 %

* Machine Learning Model 2 (Random Over Sampling):
  * Balanced Accuracy Score: 99.4%
  * Precision: Healthy Loan - 100%, Unhealthy Loan - 84%
  * Recall: Healthy Loan - 99%, Unhealthy Loan - 99 %  

## Summary

The performance of the machine learning models significantly depends on the problem we are trying to solve. In this case, where the goal is to predict whether loan will be healthy or high-risk, different aspects need to be considered.

For this particular problem, it is crucial to predict high-risk loans accurately. Misclassifying a high-risk loan as healthy could lead to substantial financial losses. Therefore, Model 2, which has a higher recall for high-risk loans (99%), is of paramount importance in this scenario. This means that Model 2 correctly identifies 99% of the high-risk loans out of all actual high-risk loans.

While precision is also important, it is usually a trade-off with recall. In this context, precision signifies the accuracy of high-risk loan predictions among all predicted high-risk loans. Model 2 has a precision of 84%, indicating that 84% of the predicted high-risk loans are accurate.

In conclusion, Model 2, developed using random oversampling, is the preferred choice for this problem. Its high recall ensures that the majority of high-risk loans are correctly identified, minimizing the risk of financial loss. However, it's essential to consider the specific business context and consequences of misclassification when choosing a model for deployment.
