# credit-risk-classification


# Module 12 Report

## Overview of the Analysis

    
The purpose of this analysis is to assess the credit risk of individuals applying for loans using our own machine learning models that we trained. The goal is to predict if an individual will be risky to loan to based on various variables. 
    
These variables are loan_size, interest_rate, borrower_income, dept_to_income, num_of_accounts, derogatory_marks, and total_dept.

Loan_status column shows either 0 or 1, 0 means that the loan is health while a 1 represents that the loan has high risk of defaulting. Defaulting means that the individual will miss payments or can't pay the loan back.
    
The main goal of the challenge is to build and evaluate our machine learning model. With a reliable model, we can help the company predict whether or not it will be risky lending to a peer.

In the first stage of the machine learning process, we split the data into training and testing sets. In this stage, we created labels set (y) from the "loan_status" column and then create the features or variables (x) from the rest of the column. The data is further split into training or testing datasets using train_test_split from sklearn. 

The second stage of the model is to create a logistic regression model. We use logistic regressio model as it is simple when working with binary classification tasks. To do that we fit the logistic regression model using training data before saving predictiong based on the testing data labels and fitted model. We then evaluate the model's performance by generating a confusion matrix and classification report.


## Results


* Logistic Regression Machine Learning Model:
    * Accuracy score of 99%
    * Precision of 100% for 0 and 84% for 1
    * Recall Scores of 99% for 0 and 94% for 1


## Summary

With the generatred confusion matric and classification report, we can determine the determine the performance of the model. And it seems that our model has an accuracy of 99% under the f1-score column. Since we do have an inbalanced dataset, we should also look at the the precision and recall column. We can say that this logistic regression model is a good model because it was able to have a 99% recall for healthy loan and 94% for high risk loans. That means that the model was able to predict 99% out of all the loans that were actually health loans. And the same goes for high risk loans though with a 94% instead. The model performs best at predicting those with health loans. Though it does not perform bad when predicting loans that will default. The performace does depend on the problem we are trying to solve. It is more important to to predict the 1 because it is better to be cautious of those that can potentially default on the loan. If they default, then it's bad for the company. Though the company should also be wary that the model does not gurantee it's prediction.




