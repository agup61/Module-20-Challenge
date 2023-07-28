# Module 20 - Credit Risk Analysis Report
![alt text](https://cdn.educba.com/academy/wp-content/uploads/2021/02/Credit-Risk.jpg)

## Overview of the Analysis
In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The purpose of this analysis is to employ a machine learning model in order to classify loans as either healthy (low-risk) or non-healthy (high-risk), based on the loan status provided by the lending company. The analysis utilizes financial information encompassing various factors, including the loan size, interest rate, borrower's income, debt-to-income ratio, number of accounts held by the borrower, derogatory marks against the borrower, total debt, and loan status.

Initially, the dataset consisting of 77,536 data points was divided into training and testing sets. Subsequently, the variables X and y were created, and the data was split using the train_test_split function. A logistic regression model, referred to as "logistic_regression_model," was then constructed using the original data and fitted with the training set. Predictions were made based on this model, and its performance was evaluated by calculating the accuracy score, generating a confusion matrix, and printing a classification report.

To address any potential class imbalance, the training data was resampled using the RandomOverSampler module from the imbalanced-learn library. This resampling technique ensured an equal representation of data points for both low-risk (75,036) and high-risk (2,500) loans. The logistic regression model was then retrained using the resampled data, following the same process as before.

The logistic regression model, implemented with the "LogisticRegression" algorithm from scikit-learn, was developed to determine the risk level of loans in the testing dataset. This algorithm was selected due to its widespread utilization in predicting the probability of a target variable in classification problems.


## Results
Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning model.

* Machine Learning Model:
  * Description of Model Accuracy, Precision, and Recall scores.
  
  The Logistic Regression Model developed using the dataset provided by the lending company achieved an impressive accuracy score of 99%. However, it is worth noting that the model's recall value for non-healthy loans (89%) is lower than the recall value for healthy loans (100%). This indicates that the model is more effective at predicting loan status as healthy rather than identifying non-healthy loans. This discrepancy can be attributed to the dataset's inherent imbalance, where healthy loans significantly outnumber non-healthy loans.
  
  The confusion matrix provides additional insights into the model's performance:
    * Out of the 18,759 loan statuses labeled as healthy (low-risk), the model accurately predicted 18,679 as healthy and misclassified 80 as healthy when they were non-healthy.
    * Out of the 625 loan statuses labeled as non-healthy (high-risk), the model correctly predicted 558 as non-healthy and incorrectly classified 67 as non-healthy when they were actually healthy.
  
  Description of the Machine Learning Model:
    * Accuracy, Precision, and Recall Scores:
    * Accuracy score: 99%
    * Healthy loans exhibit ideal precision, f1-scores, and recall rates, all reaching 100%.
    * High-risk loans display a precision rate that is 13% lower compared to healthy loans.
    * Furthermore, high-risk loans demonstrate lower recall and f1-score values, with variations of 11% and 12% respectively, when compared to healthy loans.

## Summary

Summarise the results of the machine learning models, and include a recommendation on the model to use, if any. 
  Considering the results and the objectives of the lending company, it is recommended to deploy the Logistic Regression Model for predicting loan statuses. The model's exceptional accuracy score, along with its high precision and recall for healthy loans, makes it a valuable tool for identifying low-risk borrowers. Despite a slight performance gap in detecting non-healthy loans, the model still provides meaningful insights into loan risk assessment. However, it is crucial for the company to be mindful of the imbalanced nature of the dataset, as it may impact the model's accuracy in predicting non-healthy loans reliably.

  In conclusion, the Logistic Regression Model offers a reliable and efficient approach to predict loan statuses. It effectively supports the lending company in identifying low-risk loans, facilitating informed decision-making and risk management. Continuous monitoring and adjustment, while considering the dataset's imbalance, can further enhance the model's performance in accurately identifying non-healthy loans.
