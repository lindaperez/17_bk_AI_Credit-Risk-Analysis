# Credit Risk Analysis
## Overview of the loan prediction risk analysis:

Perform a Credit risk analysis from scratch, performing the development of the solution of a unbalanced classification problem.

- It is neccesary to employ different techniques to train and evaluate models with unbalanced classes. 
- It is required to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from **LendingClub**, a peer-to-peer lending services company, It will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm.

It will be use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, It will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Finally it will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

### Resources: 
credit_risk_resampling
  Resampling Models to Predict Credit Risk
  SMOTEENN Algorithm to Predict Credit Risk

credit_risk_ensemble
  Ensemble Classifiers to Predict Credit Risk



## Results:

**Random Oversampling**

In random oversampling, instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced.

The **accuracy score** is simply the percentage of predictions that are correct. In this case, the model's accuracy score was 0.6555633473585787, meaning that the model was correct 66% of the time.


The **precision** returns the proportion of true positives among all the values predicted as positive.
From this results, the precision for a loan status low risk can be determined by the ratio TP/(TP + FP), which is 1.00. A low precision is indicative of a large number of false positives. 

There is not a high amount of false positives for category 1 (low risk). 

The **recall** returns the proportion of positive values correctly predicted. It can be determined by the ratio: TP/(TP + FN). A low recall is indicative of a large number of false negatives.

There is a large number of False negative for both categories loan status risk and high risk 66%, 67% respectively.



## Summary:

### Results Summary

### Which model to use?
