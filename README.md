# Credit_Worthiness_Model

## Overview of the Analysis

One of the problems faced with classification of Credit risk is the imbalance between healthy and risky loans. This Jupyter notebook trains and evaluates models with these imbalanced classes to identify the creditworthiness of borrowers.

### Data

The data came in the form of a csv file containing loan_size, interest_rate, borrower_income, debt_to_income, num_of_accounts, derogatory_marks, total_debt, loan_status. After reading the data into a DataFrame I seperated the target and features and used value_counts to figure out how many healthy and risky loans there were.

    Total Loan Count: 77,536
    * Healthy: 75036
    * Risky: 2500

Afterwards I split the data using train_test_split and used the LogisticRegression() to create a LogisticRegressionmodel that is fitted with the training data to use to make a prediction using the testing data. Last thing done was to analyze the prediction model using balanced_accuracy_score(), confusion_matrix(), and printing the classification_report_imbalanced(). I repeat this process one more time using the RandomOverSampler data.

## Results

* **Machine Learning Model 1:**
    * Balance Accuracy score: 95%
    * Precision: Healthy 100%/Risky 85%
    * Recall Score: Healthy 99%/Risky 91%

* **Machine Learning Model 2:**
    * Balance Accuracy score: 99%
    * Precision: Healthy 100%/Risky 84%
    * Recall Score: Healthy 99%/Risky 99%

## Summary

The result from the 2 models showed a 4% increase in accuracy score, 1% decrease in the precision of Risky loans, and a 9% increase on the recall for Risky loans. Based on the models results depending on what is needed from the model I would generally advise to use the second model because of the recall increase on risky loans which means which loans that are actually risky loans were correctly identified as risky loans. 