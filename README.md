# Credit Risk
---------------------------------------------------------------------------------------------------------
## Executive Summary
---------------------------------------------------------------------------------------------------------
In this project, I experimented with the following sampling techniques to predict which banking customers
were deemed as high-risk:

**Oversampling**                                    
* Naive Random Sampling
* Synthetic Minority Oversampling Technique (SMOTE)

**Undersampling**
* Cluster Centroid Undersampling

**Combination of Oversampling and Undersampling**
* Synthetic Minority Oversampling Technique combined with Edited Nearest Neighbors (SMOTEENN)

---------------------------------------------------------------------------------------------------------
Based on the results of the abovementioned sampling techniques, it was difficult to determine which model
was the best. The combination sampling technique (SMOTEENN) was probably the best out of the lot, but 
there was a huge disparity between the Precision and Sensitivity scores in predicting High-Risk customers.

This technique was good at ruling out High-Risk customers but the low _Precision_ score of 0.01 was indicative 
that this model falsly categorizes a large number of Low-Risk customers as High-Risk.  Therefore, in my 
opinion, I will not go with any of the models.  While, it does a good job at detecting High-Risk customers, 
arguably it does too well of a job to the extent that a large number of Low-Risk customers will be denied
access to loan facilities.  

Refer to the following link for the various steps for cleaning the data and execution of sampling methods.
https://github.com/GR8505/Credit_Risk/blob/master/Starter_Code/CR_Oversampling.ipynb

---------------------------------------------------------------------------------------------------------
## Objectives
---------------------------------------------------------------------------------------------------------
* Implement different ML models
* Use Resampling to address class imbalance
* Evaluate the performance of ML models

----------------------------------------------------------------------------------------------------------
## Resources
----------------------------------------------------------------------------------------------------------
* Python
* numpy
* pandas
* sklearn
* imblearn
* plotly

---------------------------------------------------------------------------------------------------------
## [Other Classification Methods](https://github.com/GR8505/Credit_Risk/blob/master/Starter_Code/credit_risk_ensemble.ipynb)
---------------------------------------------------------------------------------------------------------
* **Balanced Random Forest Classifier**

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/Balanced_RF1.png) | ![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_Balanced_RF1.png)
-------------------------------------------------------------------------------|------------------------------

* **Easy Ensemble Ada Boost Classifier**

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/Ada_Boost.png) | ![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_Ada_Boost.png)
----------------------------------------------------------------------------|---------------------------------

Both of these classification methods did not improve the model.  Its perfect scores for both _Precision_ and
_Recall_ when it comes to predicting Low-Risk customers is an indication of an overfitted model.  Moreover, 
the low _Recall_ score for High-Risk customers means that these methods are both prone to misclassifying a fair
amount of High-Risk customers to Low-Risk customers.

---------------------------------------------------------------------------------------------------------
## Oversampling
---------------------------------------------------------------------------------------------------------
**Naive Random Sampling**

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_Over_Sample.png)
![](https://github.com/GR8505/Credit_Risk/blob/master/Images/R_OverSample1.png)

Based on this first sampling technique, the _Precision_ for High-Risk customers is very low but _Sensitivity_
is respectable at 0.71.  _Precision for_ Low-Risk customers are too good to be true at 1. The _Recall_ score
is 0.58. Overall the accuracy of this model is good at 0.65.

----------------------------------------------------------------------------------------------------------
**SMOTE**

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_SMOTE.png)
![](https://github.com/GR8505/Credit_Risk/blob/master/Images/SMOTE1.png)

In this oversampling technique the precision scores for both High-Risk and Low-Risk customers are 
unchanged. Sensitivity score for Low-Risk customers improves slightly but declines for High-Risk customers.
Accuracy remains at 0.65.

----------------------------------------------------------------------------------------------------------
## Undersampling
----------------------------------------------------------------------------------------------------------
**Cluster Centroid Undersampling**

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_Cluster_Centroid.png)
![](https://github.com/GR8505/Credit_Risk/blob/master/Images/Cluster_Centroids1.png)

In this undersampling technique there is no significant improvement in the scores for both High-Risk and
Low-Risk customers. Furthermore, the accuracy of the model is worse at 0.54.

----------------------------------------------------------------------------------------------------------
## Combination Sampling
----------------------------------------------------------------------------------------------------------
**SMOTEENN**

![](https://github.com/GR8505/Credit_Risk/blob/master/Images/CM_SMOTEENN.png)
![](https://github.com/GR8505/Credit_Risk/blob/master/Images/SMOTEENN1.png)

This combination sampling technique yields the best Sensitivity score for High-Risk customers.  However,
there is no improvement in the Precision score for detecting High-Risk customers. The small F1 score for
High-Risk is a clear indication of the large disparity between the Precision and Sensitivity scores for
High-Risk customers.  Accuracy back up to 0.64.

----------------------------------------------------------------------------------------------------------
