# Credit-Risk-classification: Reporting

## Overview of the Analysis
Within this module, the <ins>purpose</ins> of the excercise was to train and evaluate a supervised machine learning algoright to detect loan credit worthiness. This includes the following methods:

* Financial information was based on the following  target and feature variables:
  * Features: loan_size, interest_rate,borrower_income, debt_to_income ratio, num_of_accoutns and deragotaory_marks
  * Target:  Loan_Status- 1 for High Risk and 0 for Healthy.
* Stages of the machine learning method:
1. Split the data into training and testing sets post variable determination
2. Create a Logistic Regression Model with original data
3. Save and create a prediction model with the testing data to create a predictio on loan status


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression Model with the below results metrics:
  * Accuracy: I looked at two different accuracy scores: Balanced and "normal" accuracy score
   * The balanced accuracy score, which is the average of recall within a class was used. Since, the data was imbalanced (97% of data was of healthy loan status). Therefore, the balance accruacy score was <b>94%</b>
 
   * The normal accuracy score, which tells the ratio of correctly predicted outcomes to the total number of observations, was <b>99% </b> <br>
 But, knowing that the data balance was already 97%, this is not impressive.<br>
  * Precision: The precision score measures the ratio of correctly predicted obervations to the total predicted positive observations. In this case, it was 100% for the healthy (0) status and 87% for high risk status
  * Recall Score: The recall score, which measures the ratio of correctly predicted positive observations to all predicted observation within that class. Thus,this recall score was also similar in numbers, with a score of healthy (0) was <b>100%</b> and High-Risk was <b>89%</b>
  * f1-score, which is a weighted combination of recall and precision was also in a similar range for both High Risk and Healthy. <b>100% </b> and <b>88% </b> respectively.

* Machine Learning Model 2: Logistic Regression Model with Oversampled data:
  * Accuracy: I looked at two different accuracy scores: Balanced and "normal" accuracy score
   * The balanced accuracy score, which is the average of recall within a class was used. Since, the data was now more balanced (83% of data was of healthy loan status). Therefore, the balance accruacy score improved to an <b>99%</b>
 
   * The normal accuracy score, which tells the ratio of correctly predicted outcomes to the total number of observations, was <b>99% </b> <br>
  * Precision: The precision score measures the ratio of correctly predicted obervations to the total predicted positive observations. In this case, it was 100% for the healthy (0) status and remains at 87% for high risk status
  * Recall Score: The recall score, which measures the ratio of correctly predicted positive observations to all predicted observation within that class. Thus,this recall score was also similar in numbers, with a score of healthy (0) was <b>100%</b> and High-Risk that improved to an <b>98%</b>
  * f1-score, which is a weighted combination of recall and precision also improved significantly <b>100% </b> and <b>92% </b> respectively.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. 

For the initial model: the classification report that provided the scores: precision, accuracy and recall. Along with the, balanced and "normal accu_score", we see that the model yields 95-99% accuracy of predicting the loan status correctly. However, with a sub 90% precision and recall for high risk score (Loan_status of 1). I would want to increase the data within this dataset, with the purpose of creating a more balanced dataset.

With the ultimate assumption that the model balanced accuracy also increases above a <b>98%</b> threshold and both precision and recall scores to be above <b>90%!</b>

Then, using the oversampled dataset, using the Logistically Regression Model: All the relative scores improve drastically:
balanced_accuracy_score (new 99%), recall of the high risk (98%). While the balance of recall score improves, thus improving the f1-score to 92%.
**Therefore, I would recommend this new model.**

