# Module 12 Report Template

## Overview of the Analysis

* The purpose of this analysis was to use various techniques to train and evaluate a model based on loan risk.
* A dataset of historical lending activity from a peer-to-peer lending services company was used to build a model that can identify the creditworthiness of borrowers
* In this case, the value being predicted is the `loans_status` variable. 
* A value of 0 in the `loan_status`column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
* This analysis demonstrates how resampling can help improve the performance of a model when you have an imbalanced dataset.
* The analysis compares the performance of a logistic regression model when the training dataset is resampled (using the RandomOverSampler library) and when it is not.  

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Logistic regression model with original imbalanced dataset:
  * We can observe that the performance of detecting a healthy loan is higher than a high-risk loan because there is significantly more training data for healthy loan.
  * The balanced accuracy for this model is aproximately 95%, which is pretty high considering that it is an imbalanced dataset. 
  * As expected the precision for a healthy loan is higher (100%) than a high-risk loan (85%) beacuse of the imbalanced dataset
  * Similarly, the recall for a healthy loan is higher (99%) than a high-risk loan (91%) beacuse of the imbalanced dataset.



* Logistic regression model with resampled dataset:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  * The balanced accuracy for this model has incresased after resampling the training dataset to aproximately 99%
  * We can observe that the precision for high-risk loan has decreased by 1 percent and healthy loan has stayed the same (100%). The decrease in precision for high-risk loan is due to the fact that there  are more false positives in the confusion matrix for the resampled model.
  * We can observe that the precision for high-risk loan has increased by 8 percent and healthy loan has stayed the same (99%). The increase in recall for high-risk loan is due to the fact that there are less false negatives in the confusion matrix for the resampled model.


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
