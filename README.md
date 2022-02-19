# Credit_Risk_Analysis
Challenge Assignment for Module 17

## Background
Jill commends you for all your hard work. Piece by piece, you’ve been building up your skills in data preparation, statistical reasoning, and machine learning. You are now ready to apply machine learning to solve a real-world challenge: credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.


## Purpose
The purpose of this assignment is to determine which of the six learning models demonstrated here should be used to predict credit risk. We will be testing and evaluating whether Oversampling, SMOTE oversamping, Undersampling, Combination (Over and Under) Sampling, Balanced Random Forest Classifier, or Easy Ensemble AdaBoost Classifier can and should be used to evaluate credit risk.


## Results

### Naive Random Oversampling

#### Naive Random Oversampling Dataframe
![Naive Random Oversampling Dataframe](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/NRO_cm_df.png)


#### Naive Random Oversampling Imbalanced Classification Report
![Naive Random Oversampling Imbalanced Classification Report](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/NRO_Imbalanced_Classification_Report.JPG)


* The balanced accuracy score is about .6614 or 66.14%.
* The precision score for high-risk loans is 0.01. The precision score for low-risk loans is 1.00.
* The recall score for high-risk loans is 0.60. The recall score for low-risk loans is 0.72.


### SMOTE Oversampling

#### SMOTE Dataframe
![SMOTE Dataframe](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/SMOTE_cm_df.png)


#### SMOTE Imbalanced Classification Report
![SMOTE Imbalanced Classification Report](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/SMOTE_Imbalanced_Classification_Report.JPG)


* The balanced accuracy score is about .6581 or 65.81%.
* The precision score for high-risk loans is 0.01. The precision score for low-risk loans is 1.00.
* The recall score for high-risk loans is 0.62. The recall score for low-risk loans is 0.69.

### Undersampling


#### Undersampling Dataframe
![Undersampling Dataframe](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/Undersampling_df.png)


#### Undersampling Imbalanced Classification Report
![Undersampling Imbalanced Classification Report](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/Undersampling_Imbalanced_Classification_Report.JPG)


* The balanced accuracy score is about .5441 or 54.41%
* The precision score for high-risk loans is 0.01 or 1%. The precision score for low-risk loans is 1.00 or 100%.
* The recall score for high-risk loans is 0.69 or 69%. The recall score for low-risk loans is 0.40 or 40%.


### Combination (Over and Under) Sampling

#### Combination (Over and Under) Sampling Dataframe
![Combination (Over and Under) Sampling Dataframe](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/COU_cm_df.png)


#### Combination (Over and Under) Imbalanced Classification Report
![Combination (Over and Under) Sampling Imbalanced Classification Report](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/COU_Imbalanced_Classification_Report.JPG)


* The balanced accuracy score is about .6449 or 64.49%.
* The precision score for high-risk loans is 0.01 or 1%. The precision score for low-risk loans is 1.00 or 100%.
* The recall score for high-risk loans is 0.72 or 72%. The recall score for low-risk loans is 0.57 or 57%.


### Balanced Random Forest Classifier

#### Balanced Random Forest Classifier Dataframe
![Balanced Random Forest Classifier Dataframe](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/BRFC_cm_df.png)


#### Balanced Random Forest Classifier Imbalanced Classification Report
![Balanced Random Forest Classifier Imbalanced Classification Report](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/BRFC_Imbalanced_Classification_Report.JPG)


* The balanced accuracy score is about .7885 or 78.85%.
* The precision score for high-risk loans is 0.03 or 3%. The precision score for low-risk loans is 1.00 or 100%.
* The recall score for high-risk loans is 0.70 or 70%. The recall score for low-risk loans is 0.87 or 87%.


### Easy Ensemble AdaBoost Classifier

#### Easy Ensemble AdaBoost Classifier Dataframe
![Easy Ensemble AdaBoost Classifier Dataframe](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/EEAC_cm_df.png)


#### Easy Ensemble AdaBoost Classifier Imbalanced Classification Report
![Easy Ensemble AdaBoost Classifier Imbalanced Classification Report](https://github.com/Itgotworse26/Credit_Risk_Analysis/blob/main/analysis/EEAC_Imbalanced_Classification_Report.JPG)


* The balanced accuracy score is about .9317 or 93.17%.
* The precision score for high-risk loans is 0.09 or 9%. The precision score for low-risk loans is 1.00 or 100%.
* The recall score for high-risk loans is 0.92 or 92%. The recall score for low-risk loans is 0.94 or 94%.


## Summary
As seen above, the model with the best accuracy score is the Easy Ensemble AdaBoost Classifier with a 93.17% score. Also, not only are the precision and recall scores for low-risk loans is high at 100% and 94% respectively, the precision and recall score for high-risk loans are the highest at 9% and 92% respectively. This means that the Easy Ensemble AdaBoost Classifier has a good balance between accuracy and sensitivity for assessing loans. Sensitivity is more important for credit loans is more important however, because a false positive could lead to major losses in the case of a loan incorrectly identified as low-risk. 

As a result, thanks to its accuracy score and balance between precision and recall, the Easy Ensemble AdaBoost Classifier would make a suitable model to use for assessing credit risk. 