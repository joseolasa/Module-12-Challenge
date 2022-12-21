# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis was to build a logistic Regression to classify credit risk. The logistic regressions were trained on loan data that included loan size, interest rate, debt-to-income ratio, and borrower income. The data consists of if the borrower defaulted or not. 

As part of this analysis, we followed the process below:

1. split the data, into training and testing data
2. construct the model
3. fit the model to the training data
4. predict the outcomes of the test data vs the actual test data.  

Inherent to this problem is that this data is not balanced i.e. most borrowers pay back their loans. This lack of defaulting loans will create an imbalance in our model, making it less likely to predict a correct default. Our data set has only 2500 defaults out of 77,536 data points (~3% default rate). To address the imbalance in the dataset, this analysis looks at two versions of a logistic model, one trained on the dataset as is and the other on an over-sampled dataset. In the over-sampled data, we used Random Over Sampling to create a more balanced data set artificially. We make a dataset with 112,542 points in the rebalanced model with a 50% default rate. 

* Explain the purpose of the analysis.
* Explain what financial information the data was on and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

* Machine Learning Model 1, Logistic Regression:
  * Accuracy: 0.99
  * Precision: of predicting default 0.85
  * Recall: of predicting default 0.91
  * F1: of predicting default 0.88


* Machine Learning Model 2, Logistic Regression With Over Sampling:
  * Accuracy: 0.99
  * Precision: of predicting default  0.84
  * Recall: of predicting default 0.99
  * F1: 0.91

## Summary

Overall, both models do well by predicting a default with an accuracy of ~0.99. However, the model trained with random oversampling has the best recall at 0.99 and is the recommended model. The recall value, in terms of our current model minimizes the error of not predicting a default when there actually is a default. In the case of our business, this is where we could have our greatest cost, not seeing a default when there is going to be a default. 

Additionally, the F1 score for the random oversampled model is better (0.91 vs. 0.88). The F1 score balances the risk across false positives,  false negatives, and true positives. This is also an excellent value to look at if we want to balance the risk of miss categorizing the loan. 
