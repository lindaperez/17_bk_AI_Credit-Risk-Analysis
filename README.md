# Credit Risk Analysis
## Overview of the loan prediction risk analysis:

Perform a Credit risk analysis from scratch, performing the development of the solution of a unbalanced classification problem.

- It is necesary to employ different techniques to train and evaluate models with unbalanced classes. 
- It is required to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from **LendingClub**, a peer-to-peer lending services company, It will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm.

It will be use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, It will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Finally it will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

### Resources: 
credit_risk_resampling
  * Resampling Models to Predict Credit Risk
  * SMOTEENN Algorithm to Predict Credit Risk

credit_risk_ensemble
  * Ensemble Classifiers to Predict Credit Risk



## Results:

### Oversampling **Random Oversampling**

- Accuracy: 
- Precision: 1.0
- Recall: 0.66
- F1_score: 0.79

Total Predictions 17205
Correct predictions: 11372 66.1 %
Incorrect predictions: 5833 33.9 %

* Proportion of correct predictions: **accuracy score** 66%. The **precision** from all the values predicted as positive returns the proportion of true positives among all the values predicted as positive. There is not a high amount of false positives for category 1 (loan status low risk). The **recall** returns the proportion of positive values correctly predicted. It can be determined by the ratio: TP/(TP + FN). A low recall is indicative of a large number of false negatives. There is a large number of False negative for both categories loan status risk and high risk 66%, 67% respectively, nevertheless the percentages are above 50%.

### Oversampling **SMOTE Oversampling**
**This model is less accurate than Random Oversampling**

- Accuracy: 0.65
- Precision: 1.0
- Recall: 0.65

Total Predictions 17205
Correct predictions: 11178 64.97 %
Incorrect predictions: 6027 35.03 %

* Proportion of correct predictions: **accuracy score** 65% lower that the previous model. The **Precision:** , the model is 100% reliable. **Recall:** There is a large number of False negative for both categories loan status low risk and high risk nevertheless the percetages are above 50%, 65%, 58% respectively. **F1 score:** is a weighted average of the true positive rate (recall) and precision, where the best score is 1.0 and the worst is 0.0.

### Undersampling **Cluster Centroid Undersampling**

- Accuracy: 0.48
- Precision: 1.0
- Recall: 0.48

Total Predictions 17205
Correct predictions: 8210 47.72 %
Incorrect predictions: 8995 52.28 %

* Proportion of correct predictions: **accuracy score** 48% the lower among all models. **Precision:** Same to previous models 100%. **Recall:** The numbers of false negatives in this model increased respect the previous model. The proportion of positive values correctly predicted for this model is the worst among all models.

**Combination (Over and Under) Sampling**

- Accuracy: 0.57
- Precision: 1.0
- Recall: 0.57

Total Predictions 17205
Correct predictions: 8210 47.72 %
Incorrect predictions: 8995 52.28 %

* Proportion of correct predictions: **accuracy score** 57% Lower than some previous models. The **Precision:** is same to previous models 100%. **Recall:** The proportion of positive values correctly predicted is lower than some previous models 57%.



## Summary:

### Results Summary

### Which model to use?
