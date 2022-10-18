# Module 12 Report Template

## Overview of the Analysis

The presented analysis applies a classification model, logistic regression model, to predict the creditworthiness of borrowers. The algorithm overcomes the problem with imbalanced classes by resampling the training set.

The dataset consists of over 75000 rows of numerical data on lending. We try to predict if a particular loan is going to default or not. 

There are eight financial variables in the dataset. First seven variables serve as features and the last variable 'loan_status' serve as a target variable; it is a dummy that reflects if the respective loan has high default risk.

We follow the model-fit-predict pattern. First, we select the model - logistic regression. Then we split the data into the training and testing set and fit the model to the data. Finally, we use the trained model to predict the testing set. We evaluate the accuracy of the model with balanced accuracy score, confusion matrix and classification report at the end of the analysis.

The existence of the imbalanced classes in the dataset motivates us to try resampling method (over-sampling) to even the number of datapoints in the testing and the training sets. The model trained on the resampled dataset is also evaluated and compared to the previous model that was trained on the original dataset.

## Results

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

The balanced accuracy for the first model is 92 %. By other words, the model is able to predict 92 % of the testing dataset. The precision is 100 % for the healthy loans and 85 % for the unhealthy loans. This indicator says that 100 % of the loans the model identified as healthy are actually healthy but ony 85 % the model finds as unhealthy are actually unhealthy.
The recall is 99 % for the healthy loans and 91 % for the unhealthy loans. This measure indicates that the model was able to correctly find 99 % of the healthy loans and 91 % of the unhealthy ones.

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

The balanced accuracy for the second model is 99 %. By other words, the model is able to predict 99 % of the testing dataset. The precision is 100 % for the healthy loans and 84 % for the unhealthy loans. This indicator says that 100 % of the loans the model identified as healthy are actually healthy but ony 84 % the model finds as unhealthy are actually unhealthy.
The recall is 99 % for the healthy loans and 99 % for the unhealthy loans. This measure indicates that the model was able to correctly find 99 % of the healthy loans and 99 % of the unhealthy ones.

## Summary

This analysis reveals high accuracy measures for the logistic regression models. These types of models should be considered for the prediction task. However, we have to backtest these models to prove the results are not an outcome of overfitting as the accuracy indicators are suspiciously too high.

Both models perform well, but the second model seems to be a better fit for this presented task. Since the priority of the model is not to miss any high-risk loan, the recall is a more important measure than the precision. For this reason, The second model fitted to the resampled training set is a better choice. Also, its balanced accuracy is higher for this model, 99 %, than for the first model, 92 %. 