# Credit_Risk_Analysis

##Overview of the Analysis
We used credit card dataset from LendingClub to use supervised machine learning to review credit card risk. We used RandomOverSampler and SMOrE algorithms, and under-sampled the data using the.  ClusterCentroids algorithm. SMoTEENN alogrithm was used for combinatorial approach of over-and under-sampling. Then we used reduce bais, BalancedRandomForestClassifier and EasyEnsembleClassifier, in the analysis

## Results
#### Naive Random OverSampling: 
balanced accuracy is ~0.64 meaning there is some predictive value in this model, but it is not a suitable accuracy model. Precision score is .01 for the high-risk credit profiles making the model unable to predict outcomes. The average is .62 making the model capable of predictability, but still very low for a calibrated model.

![image](https://user-images.githubusercontent.com/74630767/117556047-d991da80-b032-11eb-8007-b02f945bbc10.png)
#### SMOTE Oversampling
balanced accuracy ~0.65, very close to the Naive Random Oversampling
precision score is .01
average is .69 making the model have decent predictive capabilities
![image](https://user-images.githubusercontent.com/74630767/117556074-05ad5b80-b033-11eb-991a-19292f978445.png)

#### Cluster Centroids
balanced accuracy ~0.54, very low predictive power
precision score~0.01
average .4, the model doesn't have good predictive capabilities
![image](https://user-images.githubusercontent.com/74630767/117556089-2aa1ce80-b033-11eb-80a5-ff50690e53f8.png)

#### SMOTEENN
balanced accuracy ~0.65
precision score .01
recall score .56 which makes the model ave very low predictive capabilities
![image](https://user-images.githubusercontent.com/74630767/117556108-5755e600-b033-11eb-8d1b-636c9a1ae839.png)

#### Balanced Random Forest Classifier

![image](https://user-images.githubusercontent.com/74630767/117556116-76ed0e80-b033-11eb-8d6c-4cfdaca952fb.png)
balanced accuracy score is ~0.77, which is better than the previous 4 models tested and means there is a fair amount of predictive power in the model
precision for the high-risk credit profiles is 0.04
recall is impressive with an average recall of 0.90 indicating this is good model for predicating credit risk.
#### Easy Ensemble AdaBoost Classifier
balanced accuracy score was an impressive ~0.93 
precision is still low, albeit higher than the other models at 0.09
average recall was ~0.94
![image](https://user-images.githubusercontent.com/74630767/117556116-76ed0e80-b033-11eb-8d6c-4cfdaca952fb.png)

## Summary
Overall, the results show that the Easy Ensemble AdaBoost Classifier is the best model to test credit risk of those presented in the project. This model does have good predictive power as seen in the balanced accuracy score and the in the recall score. In all of the models, however, no one model had a good precision score for identifying high-risk credit profiles, which would be the most important function of the model. Given the high-risk profiles are a much smaller proportion of the overall data set (i.e. the data is imbalanced) precision is necessary for a model to be of use, because precision is what would allow us to pin point the high-risk credit profiles out of the large pool of good applicants. Therefore, none of these models should. Be recommended to be used to predict credit worthless.
