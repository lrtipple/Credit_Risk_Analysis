# Credit_Risk_Analysis

### Resources
jupyter, colab, LoanStats_2019Q1.csv, scikit learn, imbalanced-learn, Bootstrap

## Overview
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different
techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate 
models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler 
and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling 
using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and
EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on
whether they should be used to predict credit risk.


### Oversampling

  ####  Naive Random Sampling
  - Accuracy score: 62.5%
  - Precision score: 99%
  - Recall: 65%
  
  ![RandomOverSam_acc_Class_report](https://user-images.githubusercontent.com/99093289/173264594-6dfa1e15-803a-4dd7-8d8e-d6af2ce34b28.PNG)

  #### SMOTE Oversampling
  - Accuracy score: 65.1%
  - Precision score: 99%
  - Recall: 66%  
  ![SMOTE_Class_acc_report](https://user-images.githubusercontent.com/99093289/173264611-d413e775-f12d-420d-a269-cd232573bc32.PNG)

### Undersampling- Cluster Centroids
  - Accuracy score: 59%
  - Precision score: 99%
  - Recall: 57% 
![undersam_acc_class_report](https://user-images.githubusercontent.com/99093289/173264620-97fae7c9-1cf2-414a-b07e-e705ef502f94.PNG)

### Combination Over/Under - SMOOTEENN
  - Accuracy score: 63.8%
  - Precision score: 99%
  - Recall: 57% 
![combo_over_under_report](https://user-images.githubusercontent.com/99093289/173264637-6f2c63e7-0ea6-428b-a336-3abcd398ca4c.PNG)

### Balanced Random Forest Classifier
  - Accuracy score: 80.3%
  - Precision score: 99%
  - Recall: 86% 
![BRFC_bal_acc](https://user-images.githubusercontent.com/99093289/173264663-653245de-a8eb-42ab-9098-13ace3f7f592.PNG)
![BRFC_Class_Report](https://user-images.githubusercontent.com/99093289/173264668-ba270c5f-6eee-4667-a88c-356bbf9b5edb.PNG)

### Easy Ensemble AdaBoost Classifier
  - Accuracy score: 93.1%
  - Precision score: 99%
  - Recall: 94% 
![eec_bal_acc](https://user-images.githubusercontent.com/99093289/173264654-e363e233-b010-4a0b-ac98-1cb06dc86ff2.PNG)
![eec_Class_Report](https://user-images.githubusercontent.com/99093289/173264656-99f7d726-3b33-4fbf-9db3-635f54284f43.PNG)

## Summary
The oversampling, undersampling, and combination (SMOOTEENN) models all had a low accuracy score in the 50-60's range. Accuracy should be between 70-90%. I would not consider these machine learning models for prediction. The Easy Ensemble Classifier sampling has a 93% accuracy which is concern for overfitting the model. I would recommend using the Balanced Random Forest Classifier model as the accuracy is 80.3% 
