# Module-12-Challenge

# Files

Credit_risk_resampling - has the code used for this project. Here we look at two logistic regression models, one trained on the base data and the other with a random oversampling

Report - this is a summary of the finding from the analysis.


# Results

We trained the models on a data set that contained the following data.

![data](/Images/loan%20data.png)

This data was split using the train_test_spilt function from sklearn

For the first model, these are the results

![data](/Images/report%20m1.png)

For the second model we used a random over-sampling method to balance out the dataset
we used the sampler from imblearn.over_sampling 

The results of the second model are

![data](/Images/report%20M2.png)