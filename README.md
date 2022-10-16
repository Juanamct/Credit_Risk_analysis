# Credit_Risk_analysis

# Objective
Apply various supervised machine learning algorithms and resampling to solve a real-world challenge: credit card risk.  Using the credit card credit dataset from LendingClub (LoanStats_2019Q1.csv), a peer-to-peer lending services company, 
  1. oversample the data using the RandomOverSampler (Naive) and SMOTE algorithms 
  2. undersample the data using the ClusterCentroids algorithm 
  3. use a combination of over- and undersampling using the SMOTEENN algorithm
  4. compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 
  5. evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

# DELIVERABLE 1: OVERSAMPLING AND UNDERSAMPLING

  # Naive Random Oversampling Algorithm
  Class imbalances in Naive Random Oversampling are handled by duplicating the existing data in the minor class (high risk loan applications), and the major class (low risk loan applications).

  ![NaiveRandom_Oversample - Copy](https://user-images.githubusercontent.com/107228424/195999022-0022b613-f469-4acb-a0ad-c40c3d598960.jpg)

    Observations:
      Balanced Accuracy scores indicates:

      Recall values 

      The Precision for the low-risk loans (major class) was         , and the precision for the high-risk loans (minor class) was 

  # SMOTE Oversampling Algorithm
    Similar to Naive Random Oversampling, SMOTE Oversampling allows the minor class to match the major class in size by using k-nearest-neighbors rather than simply duplicating data.

    ![SMOTE_Oversample](https://user-images.githubusercontent.com/107228424/196053532-0cf3a661-cb73-4904-9aef-b0b57e4e4669.jpg)

    Observations:
      Observations:
      Balanced Accuracy scores indicates:

      Recall values 

      The Precision for the low-risk loans (major class) was         , and the precision for the high-risk loans (minor class)   was   compared to Naive Random Oversampling
    
# UNDERSAMPLING: 

  # ClusterCentroids Undersampling Algorithm
  
    Undersampling utilizes only actual existing data.  Some data is removed in order to do this.
    
    !![ClusterCentroids_Undersample](https://user-images.githubusercontent.com/107228424/196053025-8313552d-d1d3-4eb3-bc27-4fd4d345bd9a.jpg)
    
    Observations:
      Observations:
      Balanced Accuracy scores indicates:

      Recall values 

      The Precision for the low-risk loans (major class) was         , and the precision for the high-risk loans (minor class)   was   compared to Naive Random Oversampling
    
# DELIVERABLE 2: COMBINATORIAL SAMPLING
  
  # SMOTEENN Algorithm
  
    Put explanation
    
    !![SMOTEEN_OverUnder](https://user-images.githubusercontent.com/107228424/196053231-6ffef551-06a9-4183-92c9-c2b797fa3c1d.jpg)

    Observations:
      Observations:
      Balanced Accuracy scores indicates:

      Recall values 

      The Precision for the low-risk loans (major class) was         , and the precision for the high-risk loans (minor class)   was   compared to Naive Random Oversampling
    
# DELIVERABLE 3: ENSEMBLE CLASSIFIERS
  
  # BalancedRandomForest
  
    Put explanation
    
    !![BalancedRandomForest](https://user-images.githubusercontent.com/107228424/196053302-9d70d62e-a0db-4e12-8acc-a1e4fa2fde93.jpg)

    Observations:
      Observations:
      Balanced Accuracy scores indicates:

      Recall values 

      The Precision for the low-risk loans (major class) was         , and the precision for the high-risk loans (minor class)   was   compared to 

  # EasyEnsembleClassifier
  
    Put explanation
    
    !

    Observations:
      Observations:
      Balanced Accuracy scores indicates:

      Recall values 

      
# DELIVERABLE 4: SUMMARY OF RESULTS 


 
  
