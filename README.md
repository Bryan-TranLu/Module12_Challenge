# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of this analysis is to create a model that correctly identifies high-risk loans and healthy loans.
* The features that were assessed include loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, and total debt. The dependent variable is loan status : `0` (healthy loan) and `1` (high-risk loan)
* Initial assessment of loan status showed that there are 75036 healthy loans and 2500 high-risk loans in the dataset. There are significantly less high-risk loans compared to healthy loans to create a model.
* To address this imbalance, we initiated a random oversampler and fit the model to the original training data. The values counts were equalized at 56271 healthy loans and 56271 high-risk loans.
* A logistic regression model was used.
* Accuracy scores and data from the classification reports were compared between both models (original and oversampled).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

Note: The following metrics are to describe the predictive value to correctly classify 1 (high-risk loans).

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  * Accuracy = 0.95
  * Precision = 0.85
  * Recall = 0.91

The model has a high accuracy of 95.2% and thus is good at detecting true positives and true negatives. Precision is at 85% for the high-risk loan vs 100% for the healthy loan. The recall for the high-risk loan is 91% so the model was able to predict correctly 563 / 619 true 1 values. Looking at the F1 score, the model excels at predicting healthy loans but predicts high-risk loans 88% of the time (True positives and true negatives).

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  * Accuracy = 0.99
  * Precision = 0.84
  * Recall = 0.99
  
The oversampled model has a higher accuracy of 99.4% and thus is better at detecting true positives and true negatives. The Precision is at 84% for the high-risk loan vs 100% for the healthy loan. The recall for the high-risk loan is 99% so the model was able to predict correctly 613 / 619 true values for high-risk loans. Looking at the F1 score, the model excels at predicting healthy loans but predicts high-risk loans 91% of the time (True positives and true negatives). This is a better model than the original - there was a slight decrease in precision but a significant increase to recall.

## Summary
Machine Learning Model 2 performs best. It has the higher accuracy of 99.4% and thus is better at detecting true positives and true negatives. It also has the higher recall for high-risk loans.

In this scenario, there is more value in oversampling the minority class ("1" high-risk loans). Incorrectly classifing these clients would be costly to the firm so the 1% tradeoff in precision is worth the increase of 8% to the recall in the oversampled model. 
