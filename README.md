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
  - Analyzed accuracy and classification reports of each of the models and compared to identify best model among the 6 models.
  
## Results

  Below are the balanced accuracy and imbalanced classification reports for all 6 models. These metrics are key to understand how the models performed and evaluate the best possible models to utilize to predict risk level. 
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/AllPrecisionHighRiskLowRisk.png)
  
### 1. Oversampling - Native Random 
  
     - Accuracy is at 67.7%.
     - High Risk: Precision has a very low positivity at 1% and the recall is 76%
     - Low Risk: Precision is high at 100% and the recall is 59%
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/NaiveRandomOversampling.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/NROImbalancedClassificationReport.png)
  

  ### 2. Oversampling - SMOTE
  
     Accuracy is at 67.7%.
     High Risk: Precision has a very low positivity at 1% and the recall is 76%
     Low Risk: Precision is high at 100% and the recall is 59%
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEOversampling.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEImbalancedClassification.png)
  
  ### 3. Undersampling - Cluster Centroids
  
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/ClusterCentroidsResampler.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/Combination%20Sampling.png)
  
  ### 4. Combination (Over and Under) Sampling - SMOTEENN
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEENN.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEENNImbalancedReport.png)
  
  ### 5. Ensemble - Balanced Randon Forest Classifier
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/balancedRandomForestClassifier.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/BRFC%202.png)
  
  ### 6. Ensemble - Easy ensemble AdaBoost classifier
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/EasyEnsembleAdaBoostClassifier.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/EE_ClassificationReport.png)
  
  
  
## Analysis


Six machine learning models were used to predict bad loans for Lending Club. The Balanced Random Forest Classifier and the Easy Ensemble AdaBoost Classifier models achieved the highest scores for predicting bad loans as evidenced by their recall scores and balanced accuracy scores. Since the Easy Ensemble AdaBoost Classifier model did not generate an incremental increase in predictive value over the Balanced Random Forest Classifier model, I recommend using the Balanced Random Forest Classifier model.


Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.
