# Credit Risk Analysis
Using machine learning to predict credit risk
## Overview of the Analysis
The purpose of this project is to use six different machine learning algorithms to predict credit risk. Credit risk has an unbalanced classification problem, so different techniques are going to be used to train and evaluate models with unbalanced classes, and we are gonna determine which of the different models works best for our dataset. 
## Results. 

### Random Oversampling
This technique randomly selects instances of the minority class and adds them to the training set until the majority and minority classes are balanced.

![image](https://user-images.githubusercontent.com/104812189/199358557-ac5edd59-b36f-4d65-bf5f-8ca05336ad99.png)

The accuracy score is 66.24%, which is not high. Looking at the classification report, precision is 0.01 for the minority class (high_risk) and 1.00 for the majority class (low_risk). This means that the model is going to know each and every one of the credit holders that are 'low risk', but won't know those that may be 'high risk'. Recall is 0.7 for the minority class and 0.62 for the majority class.

### SMOTE Oversampling
In SMOTE, new instances from the minority class are interpolated. 

![image](https://user-images.githubusercontent.com/104812189/199358738-23b44a26-4f60-42d4-9f20-e996aba287da.png)

The accuracy score is 65.27%, higher than the previous technique, but still not high enough to be a good model to work with. Precision is the same as the previous report: 0.01 for the minority class (high_risk) and 1.00 for the majority class (low_risk). The model will work the same as the previous one. Recall is 0.61 for the minority class, a little lower than the previous algorithm, and 0.69 for the majority class, a little higher than the previous algorithm. 

### Cluster Centroid Undersampling
This algorithm identifies clusters of the majority class, then generates synthetic data points, called centroids, that are representative of the clusters. The majority class is then undersampled down to the size of the minority class.

![image](https://user-images.githubusercontent.com/104812189/199360968-a6829ad9-d1b9-438d-b3e8-85d8a599790f.png)

The accuracy score is 54.43%, less than each of the previous algorithms. Precision is exactly the same as the previous algorithm results. Recall is 0.69 for the minority class and 0.4 for the majority class. 

### SMOTEEN 
SMOTEENN uses a combinatorial approach of over- and undersampling, with the SMOTE and Edited Nearest Neighbors (ENN) algorithms. 

![image](https://user-images.githubusercontent.com/104812189/199361610-5073e093-9ef1-4448-8b45-2512d6e95ee9.png)

The accuracy score is 64.5%, higher than the undersampling technique, but lower than each of the oversampling algorithms.  Precision is exactly the same as all the previous algorithm results. Recall is 0.72 for the minority class and 0.57 for the majority class. 

### Balanced Random Forest Classifier
Decision tree algorithms help improve the accuracy and robustness, as well as decrease variance of the model, and therefore increase the overall performance of the model. 

![image](https://user-images.githubusercontent.com/104812189/199364232-c186871f-4280-4de2-8a2a-1d31dba483f5.png)

The accuracy score is 67.81%, better than the rest of the previous algorithms. Precision is 0.92 for the minority class and 1.0 for the majority class. Recall is 0.36 for the minority class and 1.0 for the majority class. High recall means that most of those cardholders who will actually pay back to the bank will be correctly predicted. 

### Easy Ensemble Classifier
This classifier is an ensemble of AdaBoost learners trained on different balanced boostrap samples. The balancing is achieved by random under-sampling.

![image](https://user-images.githubusercontent.com/104812189/199365084-a64de524-cfde-4838-888b-57e0d9306bad.png)

The accuracy score is 93.3%. Precision is 0.09 for the minority class and 1.0 for the majority class. Recall is 0.92 for the minority class and 0.94 for the majority class. 

## Summary
From all 6 machine learning models we can recommend the Easy Ensemble Classifier, as it resulted with an accuracy score of 93.3%, the highest from all the 6 algorithms. Although precision was low for the minority class, it is high for the majority class. Recall for both classes is high too. The highest from all algorithms. 
