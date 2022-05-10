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

- We can clearly see that the amount of low-risk information is much greater than the high-risk information, that is the reason we created a greater amount of high-risk values randomly. We confirm that both low risk and high risk are the same.

* Image #1

- Balanced accuracy is 63% which means that there is a 37% chance that it is wrong, this % is high.

* Image #2

- The confusion matrix is shown below.

* Image #3

- The precision of the model is 52/(52+5393) = 0.0096 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 52/(52+35) = 0.5977 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.5977*0.0096)/(0.5977+0.0096) = 0.0188 which means that there is no balance in precision and sensitivity.

# SMOTE Oversampling

- With the SMOTE method, we use a different methodology to equalize the values of high and low risk.

* Image #4

- Balanced accuracy is 63% which means that there is a 37% chance that it is wrong, this % is high. We can see that the results are the same as in the Random Oversampling.

* Image #5

- The confusion matrix is shown below.

* Image #6

- The precision of the model is 52/(52+5526) = 0.0093 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 52/(52+35) = 0.5977 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.5977*0.0093)/(0.5977+0.0093) = 0.0183 which means that there is no balance in precision and sensitivity.

# Cluster Centroids

- With the Cluster Centroids we use again a different methodology to equalize the values of high and low risk.

* Image #7

- Balanced accuracy is 53% which means that there is a 47% chance that it is wrong, this % is high. We can see that the results are lower than in previous techniques.

* Image #8

- The confusion matrix is shown below.

* Image #9

- The precision of the model is 53/(53+9424) = 0.0056 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 53/(53+34) = 0.6092 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.6092*0.0056)/(0.6092+0.0056) = 0.0110 which means that there is no balance in precision and sensitivity.

# SMOTEENN

- With SMOTEENN we use again a different methodology to equalize the values of high and low risk.

* Image #10

- Balanced accuracy is 63% which means that there is a 37% chance that it is wrong, this % is high. We can see that the results are the same as in some previous techniques.

* Image #11

- The confusion matrix is shown below.

* Image #12

- The precision of the model is 61/(61+7291) = 0.0083 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 61/(61+26) = 0.7011 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.7011*0.0083)/(0.7011+0.0083) = 0.0164 which means that there is no balance in precision and sensitivity.

# Balanced Random Forest Classifier

- Balanced accuracy is 78% which means that there is a 28% chance that it is wrong, this % is better than the previous ones.

* Image #13

- The confusion matrix is shown below.

* Image #14

- The precision of the model is 58/(58+1560) = 0.0358 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 58/(58+29) = 0.6667 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.6667*0.0358)/(0.6667+0.0358) = 0.0680 which means that there is no balance in precision and sensitivity.

# Easy Ensemble Classifier

- Balanced accuracy is 92% which means that there is an 8% chance that it is wrong, this % is very good. We can see that this result is the best we got from all previous techniques.

* Image #13

- The confusion matrix is shown below.

* Image #14

- The precision of the model is 79/(79+979) = 0.0747 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 79/(79+8) = 0.9080 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.9080*0.0747)/(0.9080+0.0747) = 0.1379 which means that there is no balance in precision and sensitivity.

## Summary: 
- After conducting our analysis with 6 different approaches I was able to reach the goal of detecting possible high-risk loans.
- The majority of the results were very similar, only excepting the last one which turned out to be the best.
- We should try to always use the Easy Ensemble Classifier since it brought the best results and accuracy.
- With low precision but with very high sensitivity.
- We need to make a better review of the cases for low and high risk to be able to determine whether or not it is really a loanable account or not.
    

