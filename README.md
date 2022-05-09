# Credit_Risk_Analysis

# Module 17 Challenge - Supervised Machine Learning and Credit Risk
- Employ different techniques to train and evaluate models with unbalanced classes. 
- Use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.
- Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. 
- I will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. 
- I will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 
- At the end I will evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Overview of the analysis: 
- Deliverable 1: Use Resampling Models to Predict Credit Risk
- Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
- Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
- Deliverable 4: A Written Report on the Credit Risk Analysis (README.md)

## Results: 

# Naive Random Oversampling

- We can clearly see that the amount of low risk information is much greater than the high risk information, that is the reason we created a greater amount of high risk values randomly. We confirm that both low risk and high risk are the same.

* Image #1
![Image #1](https://user-images.githubusercontent.com/95668609/167340608-d2e70763-5d49-49df-a809-5c42090f0a35.jpg)

- Balanced accuracy is 63% which means that there is a 37% chance that it is wrong, this % is high.

* Image #2
![Image #2](https://user-images.githubusercontent.com/95668609/167340617-6c3c665a-f227-4065-ada2-943d6979f9f2.jpg)

- The confusion matrix is shown bellow.

* Image #3
![Image #3](https://user-images.githubusercontent.com/95668609/167340622-3f8c5be5-14cf-4e4a-9867-4a89e27472b7.jpg)

- The precision of the model is 52/(52+5393) = 0.0096 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 52/(52+35) = 0.5977 this value is very low will exclude many possible high-risk credits.
- The f1 score is 2*(0.5977*0.0096)/(0.5977+0.0096) = 0.0188 which means that there is no balance in precision and sensitivity.
