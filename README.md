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
![Image #1](https://user-images.githubusercontent.com/95668609/167636228-2fc24bdd-f4e7-4c77-893d-6e82c2769b18.jpg)

- Balanced accuracy is 63% which means that there is a 37% chance that it is wrong, this % is high.

* Image #2
![Image #2](https://user-images.githubusercontent.com/95668609/167636246-685e663e-017b-40fd-ab3a-ddc0ed664b9f.jpg)

- The confusion matrix is shown below.

* Image #3
![Image #3](https://user-images.githubusercontent.com/95668609/167636266-afe4b9c2-c9b7-4253-81b0-437d87b0f53d.jpg)

- The precision of the model is 52/(52+5393) = 0.0096 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 52/(52+35) = 0.5977 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.5977*0.0096)/(0.5977+0.0096) = 0.0188 which means that there is no balance in precision and sensitivity.

# SMOTE Oversampling

- With the SMOTE method, we use a different methodology to equalize the values of high and low risk.

* Image #4
![Image #4](https://user-images.githubusercontent.com/95668609/167636288-486d8eea-b005-4d86-9698-c9cde28a7e16.jpg)

- Balanced accuracy is 63% which means that there is a 37% chance that it is wrong, this % is high. We can see that the results are the same as in the Random Oversampling.

* Image #5
![Image #5](https://user-images.githubusercontent.com/95668609/167636300-2daa41f5-57e2-4dd7-a1e8-1507f807239c.jpg)

- The confusion matrix is shown below.

* Image #6
![Image #6](https://user-images.githubusercontent.com/95668609/167636313-a36b0629-7c52-445c-8ca8-41399018c840.jpg)

- The precision of the model is 52/(52+5526) = 0.0093 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 52/(52+35) = 0.5977 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.5977*0.0093)/(0.5977+0.0093) = 0.0183 which means that there is no balance in precision and sensitivity.

# Cluster Centroids

- With the Cluster Centroids we use again a different methodology to equalize the values of high and low risk.

* Image #7
![Image #7](https://user-images.githubusercontent.com/95668609/167636328-ee22070c-0c6e-4eb3-9cb4-4c53db4a238d.jpg)

- Balanced accuracy is 53% which means that there is a 47% chance that it is wrong, this % is high. We can see that the results are lower than in previous techniques.

* Image #8
![Image #8](https://user-images.githubusercontent.com/95668609/167636339-ff2d3f03-a146-481c-9f57-0e0408be23e0.jpg)

- The confusion matrix is shown below.

* Image #9
![Image #9](https://user-images.githubusercontent.com/95668609/167636345-005d4f53-26eb-4c3e-aa9a-ba2e2fd346d8.jpg)

- The precision of the model is 53/(53+9424) = 0.0056 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 53/(53+34) = 0.6092 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.6092*0.0056)/(0.6092+0.0056) = 0.0110 which means that there is no balance in precision and sensitivity.

# SMOTEENN

- With SMOTEENN we use again a different methodology to equalize the values of high and low risk.

* Image #10
![Image #10](https://user-images.githubusercontent.com/95668609/167636360-add51eca-60f5-4123-9276-4c81c02bda42.jpg)

- Balanced accuracy is 63% which means that there is a 37% chance that it is wrong, this % is high. We can see that the results are the same as in some previous techniques.

* Image #11
![Image #11](https://user-images.githubusercontent.com/95668609/167636366-81e6e109-8d47-43bb-b3ec-649399d1f719.jpg)

- The confusion matrix is shown below.

* Image #12
![Image #12](https://user-images.githubusercontent.com/95668609/167636376-739ae921-9a4a-4bbd-a1b0-187a5303a2d1.jpg)

- The precision of the model is 61/(61+7291) = 0.0083 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 61/(61+26) = 0.7011 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.7011*0.0083)/(0.7011+0.0083) = 0.0164 which means that there is no balance in precision and sensitivity.

# Balanced Random Forest Classifier

- Balanced accuracy is 78% which means that there is a 28% chance that it is wrong, this % is better than the previous ones.

* Image #13
![Image #13](https://user-images.githubusercontent.com/95668609/167636391-1034b0fc-fc0d-4e6a-a367-9713e782b920.jpg)

- The confusion matrix is shown below.

* Image #14
![Image #14](https://user-images.githubusercontent.com/95668609/167636406-9dedee9e-2de5-4a4d-bb01-c6891cad3724.jpg)

- The precision of the model is 58/(58+1560) = 0.0358 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 58/(58+29) = 0.6667 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.6667*0.0358)/(0.6667+0.0358) = 0.0680 which means that there is no balance in precision and sensitivity.

# Easy Ensemble Classifier

- Balanced accuracy is 92% which means that there is an 8% chance that it is wrong, this % is very good. We can see that this result is the best we got from all previous techniques.

* Image #15
![Image #15](https://user-images.githubusercontent.com/95668609/167636420-f7eaefbe-e7c6-47cb-9a97-66d349ee1880.jpg)

- The confusion matrix is shown below.

* Image #16
![Image #16](https://user-images.githubusercontent.com/95668609/167636430-0650cec7-0329-41ea-865d-1e253a0d54b3.jpg)

- The precision of the model is 79/(79+979) = 0.0747 this value is very low and we can't be sure if it is high or low risk.
- The Sensitivity of the model is 79/(79+8) = 0.9080 this value is very low and will exclude many possible high-risk credits.
- The f1 score is 2*(0.9080*0.0747)/(0.9080+0.0747) = 0.1379 which means that there is no balance in precision and sensitivity.

## Summary: 
- After conducting our analysis with 6 different approaches I was able to reach the goal of detecting possible high-risk loans.
- The majority of the results were very similar, only excepting the last one which turned out to be the best.
- We should try to always use the Easy Ensemble Classifier since it brought the best results and accuracy.
- With low precision but with very high sensitivity.
- We need to make a better review of the cases for low and high risk to be able to determine whether or not it is really a loanable account or not.
    

