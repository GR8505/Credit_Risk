# Credit_Risk
---------------------------------------------------------------------------------------------------------
## Executive Summary
---------------------------------------------------------------------------------------------------------
### Naive Random Sampling
### Synthetic Minority Oversampling Technique (SMOTE)
### Cluster Centroid Undersampling
### Synthetic Minority Oversampling Technique combined with Edited Nearest Neighbors (SMOTEENN)
---------------------------------------------------------------------------------------------------------
Based on the results of the four sampling techniques highlighted in the appendix below, it is difficult to 
say which one is best.  The combination sampling technique (SMOTEENN) probably had the best results out of 
the lot, but there is a huge disparity between the Precision and Sensitivity scores in predicting High-Risk 
customers.

This technique is good at ruling out High-Risk customers but this low Precision score of 0.01 is indicative 
that this model falsly categorizes a large number of Low-Risk customers as High-Risk.  Therefore, in my 
opinion, I will not go with any of the models.  While, it does a good job at detecting High-Risk customers, 
arguably it does too well of a job to the extent that a large number of Low-Risk customers will be denied
access to loan facilities.  

While some may argue that denying Low-Risk customers augurs well for the lending institution, as these 
Low-Risk customers can potentially become High-Risk customers in the long-run this may not always be the 
case. 

There is a possibility that these Low-Risk customers can improve their credit standings and this can lead
to payment recoveries for the lenders in the short to medium-term.

Refer to the following link for the various steps for cleaning the data and execution of sampling methods.
https://github.com/GR8505/Credit_Risk/blob/master/Starter_Code/CR_Oversampling.ipynb

---------------------------------------------------------------------------------------------------------
### Balanced Random Forest Classifier
### Easy Ensemble Ada Boost Classifier
---------------------------------------------------------------------------------------------------------


---------------------------------------------------------------------------------------------------------
## APPENDIX
---------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------
## Oversampling
---------------------------------------------------------------------------------------------------------
### Naive Random Sampling

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_Over_Sample.png)
![](https://github.com/GR8505/Credit_Risk/blob/master/Images/R_OverSample1.png)

Based on this first sampling technique, the Precision for High-Risk customers is very low but Sensitivity
is respectable at 0.71.  Precision for Low-Risk customers are too good to be true at 1. The Recall score
is 0.58. Overall the accuracy of this model is good at 0.65.

----------------------------------------------------------------------------------------------------------
### SMOTE

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_SMOTE.png)
![](https://github.com/GR8505/Credit_Risk/blob/master/Images/SMOTE1.png)

In this oversampling technique the precision scores for both High-Risk and Low-Risk customers are 
unchanged. Sensitivity score for Low-Risk customers improves slightly but declines for High-Risk customers.
Accuracy remains at 0.65.

----------------------------------------------------------------------------------------------------------
## Undersampling
----------------------------------------------------------------------------------------------------------
### Cluster Centroid Undersampling

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_Cluster_Centroid.png)
![](https://github.com/GR8505/Credit_Risk/blob/master/Images/Cluster_Centroids1.png)

In this undersampling technique there is no significant improvement in the scores for both High-Risk and
Low-Risk customers. Furthermore, the accuracy of the model is worse at 0.54.

----------------------------------------------------------------------------------------------------------
## Combination Sampling
----------------------------------------------------------------------------------------------------------
### SMOTEENN

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_SMOTEENN.png)
![](https://github.com/GR8505/Credit_Risk/blob/master/Images/SMOTEENN1.png)

This combination sampling technique yields the best Sensitivity score for High-Risk customers.  However,
there is no improvement in the Precision score for detecting High-Risk customers. The small F1 score for
High-Risk is a clear indication of the large disparity between the Precision and Sensitivity scores for
High-Risk customers.  Accuracy back up to 0.64.

---------------------------------------------------------------------------------------------------------
## Ensemble Classifiers
---------------------------------------------------------------------------------------------------------
### Balanced Random Forest Classifier

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_Ada_Boost.png)
![]()




--------------------------------------------------------------------------------------------------------
### Easy Ensemble Ada Boost Classifier

![]()
![]()
