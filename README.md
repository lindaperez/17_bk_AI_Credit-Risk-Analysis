# Credit Risk Analysis
## Overview

Machine Learning application that aims to predict credit risk and provide a quicker and more reliable loan experience. By accurately identifying good candidates for a loan, it can help reduce default rates. The model will be trained using relevant credit data and will be designed to provide accurate predictions on whether an applicant is likely to repay the loan or not. This can help financial institutions make more informed decisions about whom to lend money to and how much to lend. Ultimately, the goal of this machine learning application is to improve the lending process and reduce the risk of default for lenders

Development Plan 

- Evaluate several Machine Learning Models to predict Credit Risk
- Using techniques like Resampling and boosting over the data
- Evaluate the performance

To address this problem, various techniques were employed to train and evaluate models with unbalanced classes. The imbalanced-learn and scikit-learn libraries were used to build and evaluate models using resampling. The credit card credit dataset from LendingClub, a peer-to-peer lending services company, was used to oversample the data using the RandomOverSampler and SMOTE algorithms, as well as undersample the data using the ClusterCentroids algorithm.

A combinatorial approach of over- and undersampling was used with the SMOTEENN algorithm. Two new machine learning models, the BalancedRandomForestClassifier and EasyEnsembleClassifier, were then compared to predict credit risk while reducing bias. Finally, the performance of these models was evaluated and a recommendation was made on whether they should be used to predict credit risk

### Resources: 
credit_risk_resampling
  * Resampling Models to Predict Credit Risk
  * SMOTEENN Algorithm to Predict Credit Risk

credit_risk_ensemble
  * Ensemble Classifiers to Predict Credit Risk

## Results:

### Oversampling **Random Oversampling**

- Accuracy: 0.66
- Precision: 1.0
- Recall: 0.66
- F1_score: 0.79

- Total Predictions 17205
- Correct predictions: 11372 66.1 %
- Incorrect predictions: 5833 33.9 %

* Proportion of correct predictions: **accuracy score** 66%. The **precision** from all the values predicted as positive returns the proportion of true positives among all the values predicted as positive. There is not a high amount of false positives for category 1 (loan status low risk). The **recall** returns the proportion of positive values correctly predicted. It can be determined by the ratio: TP/(TP + FN). A low recall is indicative of a large number of false negatives. There is a large number of False negative for both categories loan status risk and high risk 66%, 67% respectively, nevertheless the percentages are above 50%.

### Oversampling **SMOTE Oversampling**
**This model is less accurate than Random Oversampling**

- Accuracy: 0.65
- Precision: 1.0
- Recall: 0.65
- F1-score:: 0.79 

- Total Predictions 17205
- Correct predictions: 11178 64.97 %
- Incorrect predictions: 6027 35.03 %

* Proportion of correct predictions: **accuracy score** 65% lower that the previous model. The **Precision:** , the model is 100% reliable. **Recall:** There is a large number of False negative for both categories loan status low risk and high risk nevertheless the percetages are above 50%, 65%, 58% respectively. **F1 score:** is a weighted average of the true positive rate (recall) and precision, where the best score is 1.0 and the worst is 0.0.

### Undersampling **Cluster Centroid Undersampling**

- Accuracy: 0.48
- Precision: 1.0
- Recall: 0.48
- F1-score:: 0.64 

- Total Predictions 17205
- Correct predictions: 8210 47.72 %
- Incorrect predictions: 8995 52.28 %

* Proportion of correct predictions: **accuracy score** 48% the lower among all models. **Precision:** Same to previous models 100%. **Recall:** The numbers of false negatives in this model increased respect the previous model. The proportion of positive values correctly predicted for this model is the worst among all models.

### **Combination (Over and Under) Sampling**

- Accuracy: 0.57
- Precision: 1.0
- Recall: 0.57
- F1-score:: 0.72 

- Total Predictions 17205
- Correct predictions: 8210 47.72 %
- Incorrect predictions: 8995 52.28 %

* Proportion of correct predictions: **accuracy score** 57% Lower than some previous models. The **Precision:** is same to previous models 100%. **Recall:** The proportion of positive values correctly predicted is lower than some previous models 57%.

## Ensemble Learning **BalancedRandomForestClassifier**

- Accuracy: 0.92
- Precision: 0.04
- Recall: 0.61
- F1_score: 0.95

- Total Predictions 17205
- Correct predictions: 15767 91.64 %
- Incorrect predictions: 1438 8.36 %

* Proportion of correct predictions: **accuracy score** 57% Lower than some previous models. The **Precision:** is same to previous models 100%. **Recall:** The proportion of positive values correctly predicted is lower than some previous models 57%.

 ### Ensemble Learning **EasyEnsembleClassifier** 
 
- Accuracy: 0.95
- Precision: 0.1
- Recall: 0.92
- F1_score: 0.97

- Total Predictions 17205
- Correct predictions: 16403 95.34 %
- Incorrect predictions: 802 4.66 %

### Summary

### Results Summary

* The metrics of the minority class (precision, recall, and F1 score) did not improved over those of random oversampling.

* In summary, The precision for loan status low risk is high, indicating that there are not high number of false positives in all models which indicates an reliable positive classification. The recall is more than 50% for all models, which is not indicative of hight amount of false negatives. The F1 score is over 70% for some most of the models except for the undersampling, Cluster Centroid Undersampling and the combination (Over and Under) Sampling where the f1 score displayed was below 57%.


### Which model to use?

The models with best metrics reported for accuracy and f1 score and a balance percentage between precision and recall like **BalancedRandomForestClassifier**,  **EasyEnsembleClassifier** are valid candidates for sampling the data and reduce the imbalance between loan status low risk and high risk. 
