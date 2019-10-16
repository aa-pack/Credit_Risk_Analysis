# Machine Learning Homework

In the first section of homework, I have used resampling techniques from the imbalanced learn library and logistic regression classifiers to predict loan risk on data from the LendingClub.  The data will be oversampled using the Naive Random Oversampler and SMOTE algorithms.  For undersampling I use the Cluster Centroids algorithm and for the combination sampling I use the SMOTEENN algortihm.  I calculate the balanced accuracy score, a confusion matrix, and an imbalanced classification report for each sampling technique after training a logistic regression classifier on the sampled data.  Even though it wasn't mentioned in the README, I went ahead and scaled all the data using the StandardScaler.  This resulted in higher accuracy scores on my models. 

In the second section of the homework, I trained and compared two ensemble classifiers to predict loan risk on the same LendingClub data.  This data was scaled as well in order to be consisitent across models.  The two classifiers used was the balanced random forest classifier and the easy ensemble AdaBoost classifier.  A balanced accuracy score, a confusion matrix,and an imbalanced classification report was generated for each model for comparision purposes.  

## Resampling Techniques with Logistic Regression Classifiers

The model with the best balanced accuracy score was the SMOTE model at 83.89%.  It was very close to the SMOTEENN and Random OverSampler who were at 83.88% and 83.28%.  The worst model was the Clustered Centroids at 81.26%.

The SMOTE model also had the best recall score at 87% although the SMOTEENN model was very close at 86%.  The Clustered Centroids model was the worst again at 76%.

The SMOTE and SMOTEENN models had the best geometric mean scores at 84%.  The lowest score again was the Clustered Centroids model at 81%.

## Ensemble Learning 

The Easy Ensemble AdaBoost model had a balanced accuracy school of 93.3% which was considerably higher than the Balanced Random Forest Classifier at 68.3%.  

The Easy Ensemble AdaBoost model had a 92% recall score for the high risk loans while the Balanced Random Forest Classifier only had a recall of 37%.

The Easy Ensemble AdaBoost model had a geometric mean score of 93% while the Balanced Random Forest Classifier only had a score of 61%.

The top 3 features were total_pymt_inv, last_pymt_amnt, and total_rec_prncp.


## Conclusions

For this particular data, the Easy Ensemble AdaBoost model outperformed the other models with a balanced accuracy score of 93.33%, a recall of 92%, and a geometric mean score of 93%.