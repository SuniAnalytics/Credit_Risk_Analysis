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
  
     - Accuracy is at 66%.
     - High Risk: Precision has a very low positivity at 1% and the recall is 63%
     - Low Risk: Precision is high at 100% and the recall is 69%
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEOversampling.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEImbalancedClassification.png)
  
  ### 3. Undersampling - Cluster Centroids
  
     - Accuracy is at 54.4%, lower than oversampling models.
     - High Risk: Precision has a very low positivity at 1% and the recall is 69%. Similar to oversampling models.
     - Low Risk: Precision is high at 100% and the recall is 40%. Recall is lower than oversampling models.
     
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/ClusterCentroidsResampler.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/Combination%20Sampling.png)
  
  ### 4. Combination (Over and Under) Sampling - SMOTEENN
  
     - Accuracy is at 64.5%, similar to oversampling models
     - High Risk: Precision has a very low positivity at 1% and the recall is 72%. Similar to oversampling models.
     - Low Risk: Precision is high at 100% and the recall is 57%. Recall is lower than oversampling models.
     
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEENN.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/SMOTEENNImbalancedReport.png)
  
  ### 5. Ensemble - Balanced Randon Forest Classifier
 
     - Accuracy is at 78.8%, higher than all models except easy ensemble.
     - High Risk: Precision has a very low positivity at 3% (even though slightly higher than other models) and the recall is 70%. Similar to oversampling & combination models.
     - Low Risk: Precision is high at 100% and the recall is 87%, higher than all models excep Adaboost
     
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/balancedRandomForestClassifier.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/BRFC%202.png)
  
  ### 6. Ensemble - Easy ensemble AdaBoost classifier

     - Accuracy is very high at 93.1%, higher than all models.
     - High Risk: Precision and recall highest among all models. 
           Precision has a very low positivity at 9% but higher than all models. Recall is 92%.
     - Low Risk: Precision is high at 100% and the recall is 94%, highest among the models.
     
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/EasyEnsembleAdaBoostClassifier.png)
  
  ![](https://github.com/SuniAnalytics/Credit_Risk_Analysis/blob/main/images/EE_ClassificationReport.png)
  
  
  
## Summary

   Six machine learning models were used to predict bad loans for Lending Club. Each of these models used different techniques to predict high/low risk loans.
   
   1. Accuracy: The two ensemble models achieved very high accuracy scores to predict risky loans based on thier balanced accuracy scores (78.8% and 93.1%). Easy ensemble achieved highest accuracy at 93.1% 
   
   2. Low Risk Loans: All Models achieved a high precision of 100%, recall % is higher with ensemble models with Easy ensemble with 94%.
   
   3. High Risk Loans: All Models achieved a very low precision %s at <10%. Similat ro low risk loans, recall % is higher with ensemble models with Easy ensemble with 92%.
   
   ### Recommended Model:
         Easy ensemble is the preferred model to predict bad loans with its higher accuracy, precision and recall %s compared to all other models. 
         As the ability to predict high risk loans is important for the lending business, we need to explore futher to identify models that can improve precision for high risk loans as none of the current 6 options provide a good precision %. 
