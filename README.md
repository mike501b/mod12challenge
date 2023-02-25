# Module 12 Report

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).


The purpose of this analysis was to compare the performance of a Logistic Regression model on original data versus when the data is resampled using the "RandomOverSampler" function.
The data we used was lending data with various features such as loan size, interest rate, borrower income, debt_to_income and a "y" column that marks whether the loan is considered healthy or 'high-risk'.
Using the 'train_test_split' function we split out in-sample and out-of-sample data. We fit the Logistic Regression model with the training data (in-sample) and predicted on the testing data (out-of-sample).

The next step was to use the 'RandomOverSampler' so that the number of healthy and high risk loans were the same. We repeated the proccess of fitting the model with the resampled data and predicting on it.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * balanced accuracy score: 99.4%
  * precision:
      * Healthy Loan: 100%
      * High risk loan: 85%
  * Recall:
      * Healthy Loan: 99%
      * High risk loan: 91%


* Machine Learning Model 2:
  * balanced accuracy score: 95.2%
  * precision:
      * Healthy Loan: 100%
      * High risk loan: 84%
  * Recall:
      * Healthy Loan: 99%
      * High risk loan: 99%

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
The model using the resampled data works the best. Precision is more or less the same and recall increased from 85% to 99% with the resampled data. This means that the model was better at correctly predicting high-risk loans

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

For this problem it seems like it is more important to accurately predict high risk loans than healthy loans because high risk loans can cause a loss of money. Falsely predicting a healthy loan is high risk means the loan won't be taken and no money will be made or lost. 
