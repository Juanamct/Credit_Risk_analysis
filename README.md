# Credit_Risk_analysis

# Objective
Apply various supervised machine learning algorithms and resampling to solve a real-world challenge: credit card risk.  Using the credit card credit dataset from LendingClub (LoanStats_2019Q1.csv), a peer-to-peer lending services company, 
  1. oversample the data using the RandomOverSampler (Naive) and SMOTE algorithms 
  2. undersample the data using the ClusterCentroids algorithm 
  3. use a combination of over- and undersampling using the SMOTEENN algorithm
  4. compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 
  5. evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

# DELIVERABLE 1: OVERSAMPLING (the smaller class is resampled to make it larger) AND UNDERSAMPLING (the size of the majority class is decreased)

  # Naive Random Oversampling Algorithm
  Class imbalances in Naive Random Oversampling instances of the minority class are randomly selected and added to the training set until the majority 
  and minority classes(high risk loan applications) are balanced.  Random oversampling draws from existing observations.

  ![NaiveRandom_Oversample - Copy](https://user-images.githubusercontent.com/107228424/195999022-0022b613-f469-4acb-a0ad-c40c3d598960.jpg)

    Naive Random Oversampling Observations:
      Balanced Accuracy scores indicates: .66077 which does not lead me to recommend this model as worked

      Recall/sensitivity value of .72 for the high risk class is okay

      The Precision for the high-risk loans (minor class) was very low at .01  

  # SMOTE Oversampling Algorithm
    Similar to Naive Random Oversampling, SMOTE Oversampling the size of the minority is increased. In SMOTE, new instances are interpolated. 
    For an instance from the minority class, a number of its closest neighbors is chosen. Based on the values of these neighbors, new values 
    are created.  Smote generates synthetic observations.

   ![SMOTE_Oversample](https://user-images.githubusercontent.com/107228424/196053736-d149be6e-d931-4c0c-919f-d784d7dae57e.jpg)
 

    SMOTE Oversampling Observations:  Identical to the NaiveRandom model.
      Balanced Accuracy scores indicates: .66077 which does not lead me to recommend this model as worked

      Recall/sensitivity value of .72 for the high risk class is okay

      The Precision for the high-risk loans (minor class) was very low at .01 
    
# UNDERSAMPLING: Undersampling utilizes only actual existing data.  

  # ClusterCentroids Undersampling Algorithm
    Undersampling is another technique to address class imbalance. 
    Instead of increasing the number of the minority class, the size of the majority class is decreased.
    
   !![image](https://user-images.githubusercontent.com/107228424/197423999-09bfe603-31e9-4dbf-ba06-74f69e877452.png)


    ClusterCentroids Undersampling Observations:  Lower results than the 2 oversampling methods
      Balanced Accuracy scores indicates:  .544237 which does not lead me to recommend this model as worked

      Recall/sensitivity value of .69 for the high risk class is lower than oversampling models and okay

      The Precision for the high-risk loans (minor class) was the same as the oversampling methods, very low at .01 
    
# DELIVERABLE 2: COMBINATORIAL SAMPLING
  
  # SMOTEENN Algorithm
  
    SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms. SMOTEENN is a two-step process: 
    1.	Oversample the minority class with SMOTE.
    2.	Clean the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong 
    to two different classes, that data point is dropped.

    
   !![image](https://user-images.githubusercontent.com/107228424/197424078-7dbafbf4-aaa2-430a-b054-5d092794a0c5.png)

    
    SMOTEEN Combinatorial Observations:  Accuracy score lower than the under and over sampling methods
      Balanced Accuracy scores indicates:  .544237 which does not lead me to recommend this model as worked

      Recall/sensitivity value of .74 for the high risk class is higher than oversampling and undersampling models

      The Precision for the high-risk loans (minor class) was the same as the oversampling and unsampling methods, very low at .01 
    
# DELIVERABLE 3: ENSEMBLE CLASSIFIERS - combining multiple models, like decision tree algorithms, to help improve the accuracy and 
robustness, as well as decrease variance of the model, and therefore increase the overall performance of the model
  
  # BalancedRandomForest
  
    A random forest algorithm will sample the data and build several smaller, simpler decision trees. Each tree is simpler because it 
    is built from a random subset of features.  Combining a decision tree with more decision trees—all using different training and testing sets.
    
   ![BalancedRandomForest](https://user-images.githubusercontent.com/107228424/196053854-91575aa2-cb4a-49d1-8c0e-5f6c630e84d0.jpg)


    BalancedRandomForest Ensemble Observations:  Very strong accuracy score.  Best of all the methods
      Balanced Accuracy scores indicates: a very strong score of .9959
      
      Recall/sensitivity value of .37 for the high risk class which is lower than oversampling and undersampling models

      The Precision for the high-risk loans (minor class) is .88 which is much higher than the other models. 
    
  # EasyEnsembleClassifier
  
   ![image](https://user-images.githubusercontent.com/107228424/197424141-a158e104-8c2e-4147-a534-4027830ebead.png)
    
    EasyEnsemble Observations:  Much lower accuracy scorethan the BalancedRandom Forest.
      Balanced Accuracy scores indicates: a not confident building score of .683022
  
      Recall/sensitivity value of .37 for the high risk class which is lower than oversampling and undersampling models

      The Precision for the high-risk loans (minor class) is .88 which is much higher than the other models. 

# DELIVERABLE 4: SUMMARY OF RESULTS 

    F1 Scores for the Oversampling, Undersampling and Combinatorial methods were very low at .01 - .02 for high-risk loans class.
    F1 Score for BalancedRandomForest was much better at .52 which indicates a better balance between precision and sensitivity.
    
    Precision for the best using the BalancedRandomForestEnsemble method and EasyEnsemble methods.  
    
    Recommendation: I would recommend using the BalancedRandomForest Ensemble method since I believe precision in more important than 
    sensitivity for this application.  It's precision score is good (better than the other methods), and it's Accuracy and F1 scores 
    are much higher.  I would recommend reevaluating the data though, and rerunning the data to get better precision.

 
  
