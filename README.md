# Credit_Risk_analysis

# Objective
Apply various supervised machine learning algorithms and resampling to solve a real-world challenge: credit card risk.  Using the credit card credit dataset from LendingClub (LoanStats_2019Q1.csv), a peer-to-peer lending services company, 
  1. oversample the data using the RandomOverSampler (Naive) and SMOTE algorithms 
  2. undersample the data using the ClusterCentroids algorithm 
  3. use a combination of over- and undersampling using the SMOTEENN algorithm
  4. compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 
  5. evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

# OVERSAMPLING

  # Naive Random Oversampling
  Class imbalances in Naive Random Oversampling are handled by duplicating the existing data in the minor class (high risk loan applications), and the major class (low risk loan applications).

  ![NaiveRandom_Oversample - Copy](https://user-images.githubusercontent.com/107228424/195999022-0022b613-f469-4acb-a0ad-c40c3d598960.jpg)

    Observations:
      Balanced Accuracy scores indicates:

      Recall values 

      The Precision for the low-risk loans (major class) was         , and the precision for the high-risk loans (minor class) was 

    # SMOTE Oversampling
    Much like the Naive Random Oversampling, SMOTE Oversampling allows the minor class to match the major class in size by using k-nearest-neighbors rather than simply duplicating data.

    !![SMOTE_Oversample](https://user-images.githubusercontent.com/107228424/195999211-1487516c-5ce8-42fc-b3ca-61f4d97ba56c.jpg)

    Observations:
      Observations:
      Balanced Accuracy scores indicates:

      Recall values 

      The Precision for the low-risk loans (major class) was         , and the precision for the high-risk loans (minor class)   was 
    
    # 
  
