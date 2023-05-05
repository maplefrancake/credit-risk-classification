# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

For this challenge, I created two models with different method to classify loans as either healthy or high risk. The financial information driving these models were on lending data, which included data such as:
  * Loan size
  * Interest rate
  * Debt-to-income ratio
  * and more...

The models were attempting to predict the 'loan status' of each loan, which means whether it was healthy or a high-risk loan. As part of the analysis, I split up the given data into training and test sets, fit a logistic regression model with the training set, predicted the outcomes for the test points, and compared these predictions to the actual loan status. For the second model, I used a random oversampling method to resample the data to have an equal number of healthy and high risk loans used to train the model. I worked through the same steps and compared how well this model did to the first first one.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced accuracy: 0.9218
 
  |  | Precision | Recall |
  | --- | --- | --- |
  | Healthy | 1.00 | 0.99 |
  | High-risk | 0.85 | 0.91 |



* Machine Learning Model 2:
  * Balanced accuracy: 0.9205
  
  |  | Precision | Recall |
  | --- | --- | --- |
  | Healthy | 1.00 | 0.99 |
  | High-risk | 0.84 | 0.99 |

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
  * For overall classification, the first machine learning model performs better than the second, as its balanced accuracy is slightly higher than that of the second model. Either model would work in this scenario, as they both have high accuracy, precision, and recall. The first model just barely outperforms the second.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
  * In our case, I believe performance does matter, as we are wanting to identify and act upon high-risk loans. Therefore, predicting the `1`'s should be considered higher priority. The first model predicts correctly 85% of the time, while the second predicts correctly 84% of the time. On the flip side, of all high-risk loans, the first model classifies them properly 91% compared to 99% for the second model. Either one of these models would work for this case.
* If you do not recommend any of the models, please justify your reasoning.
