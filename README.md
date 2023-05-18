# Module 12 Report Template

## Overview of the Analysis

* The purpose of this analysis was to use various techniques to train and evaluate a model based on loan risk.
* A dataset of historical lending activity from a peer-to-peer lending services company was used to build a model that can identify the creditworthiness of borrowers
* In this case, the value being predicted is the `loans_status` variable. 
* A value of 0 in the `loan_status`column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
* This analysis demonstrates how resampling can help improve the performance of a model when you have an imbalanced dataset.
* The analysis compares the performance of a logistic regression model when the training dataset is resampled (using the RandomOverSampler library) and when it is not.  

## Results

* Logistic regression model with the original imbalanced dataset:
  * We can observe that the performance of detecting a healthy loan is higher than a high-risk loan because there is significantly more training data for the healthy loan.
  * The balanced accuracy for this model is approximately 95%, which is high considering that it is an imbalanced dataset. 
  * As expected, the precision for a healthy loan is higher (100%) than for a high-risk loan (85%) because of the imbalanced dataset
  * Similarly, the recall for a healthy loan is higher (99%) than for a high-risk loan (91%) because of the imbalanced dataset.
![LRM_original]()


* Logistic regression model with the resampled dataset:
  * The balanced accuracy for this model has increased after resampling the training dataset to approximately 99%
  * We can observe that the precision for the high-risk loans has decreased by 1 percent, and the healthy loans have stayed the same (100%). The precision decreased for high-risk loans because there are more false positives in the confusion matrix for the resampled model.
  * We can observe that the precision for high-risk loans has increased by 8 percent, and healthy loans have stayed the same (99%). The increase in recall for high-risk loans is due to fewer false negatives in the confusion matrix for the resampled model.
![LRM_resampled]()

## Summary


* Although the precision for high-risk loans has decreased by 1% for the Logistic regression model with the resampled dataset, we can observe that the balanced accuracy has increased. The model performs better overall with higher precision and f1-score for high-risk loans.
* Choosing the correct model for the task will depend on the importance of the prediction. In our case, importance is given to the model that's better at predicting high-risk loans (`1`). 
* Not enough information was given to decide which wrong scenario in the confusion matrix is given more importance, but based on my understanding, it will generally be better for the model to have fewer false negatives (predicting that a loan is healthy when it is actually not) than false positives (predicting that the loan is of high-risk when it is actually not). Therefore, the logistic regression model with the resampled dataset is a better choice out of the two for this purpose.
