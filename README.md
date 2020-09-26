# Credit_Risk
---------------------------------------------------------------------------------------------------------
## Executive Summary
---------------------------------------------------------------------------------------------------------
Based on the results of the four sampling techniques highlighted below, it is difficult to say which one 
is best.  The combination sampling technique (SMOTEENN) probably had the best results out of the lot, but
there is a huge disparity between the Precision and Sensitivity scores in predicting High-Risk customers.

This technique is good at ruling out High-Risk customers but this low Precision score of 0.01 is indicative 
that this model falsly categorizes a large number of Low-Risk customers as High-Risk.  Therefore, in my 
opinion, I will not go with any of the models.  While, it does a very good job at detecting High-Risk 
customers, it does too well of a job to the extent that a large number of Low-Risk customers will be denied
access to loan facilities.  

While some may argue that denying Low-Risk customers augurs well for lenders, as these customers can 
potentially become High-Risk customers, this may not be the case. A good portion of these Low-Risk customers 
can rebound and lenders often recover these debt collections in the short to medium-term.

---------------------------------------------------------------------------------------------------------
## Oversampling
---------------------------------------------------------------------------------------------------------
### Naive Random Sampling

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_Over_Sample.png)
![](https://github.com/GR8505/Credit_Risk/blob/master/Images/R_OverSample.png)

Based on this first sampling technique, the Precision for High-Risk customers is very low but Sensitivity
is respectable at 0.71.  Precision for Low-Risk customers are too good to be true at 1. The Recall score
is 0.58. Overall the accuracy of this model is good at 0.65.


### SMOTE

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/SMOTE.png)

In this oversampling technique the precision scores for both High-Risk and Low-Risk customers are 
unchanged. Sensitivity score for Low-Risk customers improves slightly but declines for High-Risk customers.
Accuracy remains at 0.65.

----------------------------------------------------------------------------------------------------------
## Undersampling
----------------------------------------------------------------------------------------------------------
### Cluster Centroid Undersampling

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/Cluster_Centroids.png)

In this undersampling technique there is no significant improvement in the scores for both High-Risk and
Low-Risk customers. Furthermore, the accuracy of the model is worse at 0.54.

----------------------------------------------------------------------------------------------------------
## Combination Sampling
----------------------------------------------------------------------------------------------------------
### SMOTEENN

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/SMOTEENN.png)

This combination sampling technique yields the best Sensitivity score for High-Risk customers.  However,
there is no improvement in the Precision score for detecting High-Risk customers. The small F1 score for
High-Risk is a clear indication of the large disparity between the Precision and Sensitivity scores for
High-Risk customers.  Accuracy back up to 0.64.

---------------------------------------------------------------------------------------------------------
