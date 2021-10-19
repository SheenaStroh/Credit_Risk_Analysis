# Credit Risk Analysis

## Overview
A new peer-to-peer lending service wants to use machine learning to analyze existing lending data and estimate credit risk. Using a credit card dataset from LendingClub I will run various sampling algorithms, and review the performance of each one to determine if they can reasonably be used to predict credit risk. The data is extremely unbalanced, the good loans far outweigh the bad, so I will have to use several different techniques for unbalanced data.

## Results
I used six different methods to evaluate this data, first I oversampled using random oversampling and SMOTE algorithms, then undersampled using a cluster centroids algorithm, used a combination of under and oversampling utilizing a SMOTEENN algorithm, and finally used two different types of ensemble classifiers, the balanced random forest and easy ensemble classifiers.
Naive Random Oversampling
  - Balanced accuracy score: 0.666
  - Precision and Recall scores:
   ![Oversampling_Report](https://user-images.githubusercontent.com/85318060/137845655-d313c3fe-ba1f-4d72-ad80-f44a0d21c2c8.png)

SMOTE Oversampling
 - Balanced accuracy score: 0.662
 - Precision and Recall scores:
 ![SMOTE_Report](https://user-images.githubusercontent.com/85318060/137845805-45449743-67c9-4f5d-9956-4f50d2bcf3ba.png)

Undersampling
 - Balanced accuracy score: 0.544
 - Precision and Recall scores:
 ![Undersampling_Report](https://user-images.githubusercontent.com/85318060/137845884-a74ea85d-5aa1-4b68-927e-ea39f6d14c52.png)

SMOTEENN Combination Sampling
 - Balanced accuracy score: 0.645
 - Precision and Recall scores:
 ![Combination_Report](https://user-images.githubusercontent.com/85318060/137845982-5c4458b7-daa0-4afa-a234-e6706b1b686a.png)

Balanced Random Forest Classifier
 - Balanced accuracy score: 0.789
 - Precision and Recall scores:
 ![BalancedRandomForest_Report](https://user-images.githubusercontent.com/85318060/137846083-53d4c2f3-1b98-48e4-ac31-bb7dd42a6bdf.png)

Easy Ensemble Classifier
 - Balanced accuracy score: 0.932
 - Precision and Recall scores:
 ![EasyEnsemble_Report](https://user-images.githubusercontent.com/85318060/137846158-b3c09005-cc55-4271-808b-eafec1cc2ec4.png)

## Summary
Overall none of the given sampling methods worked well for analyzing credit risk. They all work fairly well for predicting good credit applications, though with a precision score of 1.0 they were likely somewhat overfit. Unfortunately the best precision score was only 0.09 on the easy ensemble classifier. While that is an extremely marked improvement from the other sampling methods, it still does not seem like a good enough value to risk using them to predict credit risk.
