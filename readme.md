# In this project, we focused on Ecommerce data to predict the purchase behavior
## This project is done using GoogleColab.

### 1. Data exploration
### 2. Feature engineering
Informational duration show very few yes data for revenue.
Other featurs show more or less the same pattern for yes and no.
Imbalanced data should be taken into consideration before training models.

### 3. Data subsampling

### 4. Classification models: Logistic regression, SVM, RandomForest
* 1. With subsampling, logistic regression shows higher recall for class 'True', 
    it can predict 100% for class 'True' which is important. However, for class  'False' it is 0%, means it is really bad to predict 'false' class.

* 2. With or without subsampling, linear SVM shows exact the same recall 100% which is a good model. However, the recall for 'false' class is 0%

* 3. Random forest shows page values, Month and administrative duration show the most import features. The f1 score is higher than the logistic regression and SVM.

### 5. Performance check for models
* Subsampling not showing a better performance for all three classifiers.
* n-estimators 50 and above shows the same performance score for RandomForest classifier.

### 6. Clustering with KMean, semi-supervising model
* 6.1 Use number of inertia and cluster to determin 'elbow'.
* 6.2 visulize different cluster number for different features
* 6.4 Hierarchy visulization of the structure
* 6.5 Conclusion: KMeans clustering shows a better cluster behavior when cluster number equals 4

### 7. Semi-supervised learning. 
* Use June-September data to predict October-December revenue.
* use normalized values for numeric features to avoid outlier 'drawing effect' *

#### 7.3 Conclusion:
* Self-labeled data gave worse recall and f1 score than original data. 
* Low recall, i.e.'true' class predition are low for both. For self-labeled data, it is ~40% lower than original data.
* Both methods showed the similar precision and 'False' class recall rate. 
* If we have missing data, semi-supervised learning could be good method to use.
* Feature importance varies depend on what data to use.