# Credit_Risk_Analysis
## Overview

In this project, we were tasked with understanding whether a credit card loan application should be viewed as high or low risk. To do this, we are going to use the credit card credit dataset from LendingClub, a peer-to-peer lending services company. A crucial part of understanding this project is recognizing that credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. To counteract this and understand the efficacy of resampling, we will use 4 different resmpling methods. After that, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

## Results

In the proccess os resampling, we executed the following steps:
1. Resampled the dataset
2. Checked the balance of our target values
3. Trained the Logistic Regression model using the resampled data
4. Calculated the balanced accuracy score
5. Displayed the confusion matrix
6. Printed the imbalanced classification report

In the below charts, the way to read the Precision and Sensitivity chart is as follows:
Precision for high risk applications, precision for low risk application, sensitivity for high risk applications, sensitivity for low risk applications
|                 | Pre                   | Rec  |
| :-------------: |:-------------:        | :-------------:|
| High Risk       | Precision for high risk applications |  Sensitivity for high risk applications |
| Low Risk        | Precision for low risk applications |  Sensitivity for low risk applications |

### Resampling Results

| Resampling Type      | Accuracy Score                                            | Precision and Sensitivity  |
| :-------------:      |:-------------:                                            | :-------------:|
| Oversampling         | ![oversample_acc.png](Resources/oversample_acc.png)   | ![oversampling_matrix.png](Resources/oversampling_matrix.png) |
| SMOTE Oversampling   | ![somte_acc.png](Resources/somte_acc.png)                 | ![smote_matrix.png](Resources/smote_matrix.png) |
| Undersampling        | ![undersampling_acc.png](Resources/undersampling_acc.png) | ![undersampling_matrix.png](Resources/undersampling_matrix.png) |
| Combination Sampling | ![combo_acc.png](Resources/combo_acc.png)                 | ![combo_matrix.png](Resources/combo_matrix.png) |


### Ensemble Results
| Ensemble Type      | Accuracy Score                          | Precision and Sensitivity  |
| :-------------:    |:-------------:                          | :-------------:|
| Random Forest      | ![brf_acc.png](Resources/brf_acc.png)   | ![brf_matrix.png](Resources/brf_matrix.png) |
| Easy Ensemble      | ![eec_acc.png](Resources/eec_acc.png)   | ![eec_matrix.png](Resources/eec_matrix.png) |

## Summary

In looking at the results produced by the two ensemble models, we can pinpoint the Easy Ensemble Adabook Classifier as the best performing model. We can categorize it as such by looking at the accuracy and sensitivity scores with regards to high risk applications. In these categories, it outperformed the Balanced Random Forest Classifier. 

Due to Easy Ensemble Adabook Classifier's outperformance, I believe it is the model that is worth using. The high sensitivity score ensures that it will find more high risk applications than may actually exist, but in my mind it is better to play it safe with loans. 
