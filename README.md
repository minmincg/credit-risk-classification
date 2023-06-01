
## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of this analysis was to predict high risk loans and healthy loans. Also, we wanted to know with which certainty we could
trust the model to have a good prediction.
* We used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the
creditworthiness of borrowers.
* For our prediction we will use a value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
* For this machine learning process I followed the following steps:
        1.- Read the CSV data into a Pandas DataFrame.¶.
        2.- EXTRACTED the inormation from my target column as y and made the rest of the data to X.
        3.- I checked the balance of the target variable (y) by using the value_counts function.
        4.- Fit a logistic regression model
        5.- Save the predictions on the testing data labels
        6.-  Evaluate the model’s performance by doing the following:
            Calculate the accuracy score of the model.

            Generate a confusion matrix.

            Print the classification report.
* For this analysis we used the Logistic Regression Model. This model gives each data point a probability of being in the 1 category, depending on where the point is in the graph, the model will return on which side of the graph it is, on the 0's side, or on the 1's side. 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Logistic Regression Model:
 We predicted both the 0 (healthy loan) and 1 (high-risk loan) labels with the original data and this is how our model performed:

100% of the times we predicted a healthy loan, it was TRUE, and we were able to find all healthy loans. The model got an f1-score of 100% Which is awesome.

Though, only 87% of the times we predicted high-risk loans, they were True (we mistakingly let go of 13% of the loans, which still is pretty good because we were right about HIGH RISK loans 87% of the times. We were able to find 89% of the high risk loans and got an 88% on the f1-score.

Overall a good model, I would use this since we want to AVOID high risk loans.



* Machine Learning Model 2:
  * 100% of the times we predicted a healthy loan, it was TRUE, and we were able to find all healthy loans. The model got an f1-score of 100% Which is awesome.

Though, only 87% of the times we predicted high-risk loans, they were True (we mistakingly let go of 13% of the loans, which still is pretty good because we were right about HIGH RISK loans 87% of the times. We were able to find 100% of the high risk loans and got an 93% on the f1-score.

Overall a better model than the one with the original data, I would use this one instead since we want to AVOID high risk loans and this one is better at finding high risk loans.

## Summary

Both models are very similar with the difference that in the second one we fitted with oversampled data. This model overall did a better job than the one with the original data. I would use Logistic Regression Model with Resampled Training Data to make predictions, since we want to AVOID high risk loans and this one is better at finding high risk loans. 

