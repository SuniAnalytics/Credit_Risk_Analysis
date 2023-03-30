# Credit_Risk_Analysis

## Overview

  Objective of the project is to utilize supervised machine learning models to predict credit card loan's risk level (Low/High). 
  As part of the project, we need to evaluate all the factors from the data set that can help predict a loan with low/high risk category. 
  
  This reqiures utilizing machine learning, statistical analysis and evaluation of multiple models. 
  
  Followed below steps to identify best possible model to use to predict credit risk among the 6 ML models:
  - Read the data, data cleanup
  - Split data to train and test data
  - Oversampling models (Naive Random, SMOTE)
  - Undersampling model (Cluster Centroids)
  - Combination sampling (SMOTEEN)
  - Ensemble Models to minimize bias (Balanced Randon Forest Classifier, Easy ensemble AdaBoost classifier)
  
## Results

  Below are the balanced accuracy and imbalanced classification reports for all 6 models. These metrics are key to understand how the models performed and evaluate the best possible models to utilize to predict risk level. 
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/AllPrecisionHighRiskLowRisk.png)
  
  ### Oversampling - Native Random 
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/NaiveRandomOversampling.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/NROImbalancedClassificationReport.png)
  

  ### Oversampling - SMOTE
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEOversampling.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEImbalancedClassification.png)
  
  ### Undersampling - Cluster Centroids
  
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/ClusterCentroidsResampler.png)
  
  ### Combination (Over and Under) Sampling - SMOTEENN
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEENN.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEENNImbalancedReport.png)
  
  ### Ensemble - Balanced Randon Forest Classifier
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/balancedRandomForestClassifier.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/BRFC_ClassificationReportImbalanced.png)
  
  ### Ensemble - Easy ensemble AdaBoost classifier
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/EasyEnsembleAdaBoostClassifier.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/EE_ClassificationReport.png)
  
  
  
## Analysis


Six machine learning models were used to predict bad loans for Lending Club. The Balanced Random Forest Classifier and the Easy Ensemble AdaBoost Classifier models achieved the highest scores for predicting bad loans as evidenced by their recall scores and balanced accuracy scores. Since the Easy Ensemble AdaBoost Classifier model did not generate an incremental increase in predictive value over the Balanced Random Forest Classifier model, I recommend using the Balanced Random Forest Classifier model.


Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.
