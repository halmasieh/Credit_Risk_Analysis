# Credit_Risk_Analysis

## Project Overview
All around the world, people borrow money to produce cars, homes, start bussinesses and persue education.
Loans are essential part of modern society and present an opportunity and challenge for bank and another 
lender institutions. On one hand, loans create revenue with the interest rate generated, on the other hand, there is a risk of not paying people and lenders may loose money. Banks rely on income, credit scores and people's assets to reduce the risk. By increasing the financial technologies and using machine learning, bank can analyze this risk. Machine learning can process data to receive a single decision. 

This analysis can be summarized in the following steps, using machine learning:
- Use Python and Scikit-learn to predict credit risk.
- Compare the strengths and weaknesses of machine learning models.
- Assess how well a model classsifies and predicts data.

In addition, we apply resampling skills as well as build on old skills. These skills are important because machine learning requires to think about all the pieces of the data analytics puzzle at once. In fact, machine learning requires to think about people's aspects to the puzzle too. After all, the best analysis is not worth much if the stakeholders do not understand. We dig into the technical details and the puzzle pieces, to several machine learning models and evaluate them to predict credit risk, and being able to predict credit risk with machine learning algorithms can help banks and financial institutions predict anomalies, reduce risk cases, monitor portfolios, and provide recommendations on what to do in cases of fraud.


## Resources
Software: [Python 3.7.6](https://www.python.org/downloads/) and [Jupyter Notebook](https://www.anaconda.com/products/individual)

library: Scikit-learn


## Results
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Lastly, we’ll evaluate the performance of these models to be used to predict credit risk.

## Use Resampling Models to Predict Credit Risk

1-As shown in the following table,





<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Naive-Random-Oversampling.PNG" width="700" height="600"/>




The metrics for the majority class are as follows:
- Precision: 1
- Recall: 0.61
- F1 Score: 0.76
- Model's Accuracy: 0.60
- Balanced Accuracy Score: 0.65
 
From the confusion matrix results, the precision ("pre" column) is low, indicating a large number of false positives, which indicates an unreliable positive classification. The recall ("rec" column) is also low,  which is indicative of a large number of false negatives. The F1 score is also not so high. In summary, this random forest model is not good at classifying low risk because the model's accuracy and F1 score are low. In addition due to the very low precision and F1 score, this model is not a good classifier for high risk as well. 


2- As shown in the following table,





<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/SMOTE-Oversampling.PNG" width="700" height="600"/>




The metrics for the majority class are as follows:
- Precision: 1
- Recall: 0.69
- F1 Score: 0.82
- Model's Accuracy: 0.69
- Balanced Accuracy Score: 0.66

The precision ("pre" column) and recall ("rec" column) are not high for both the majority and minority class. Compared to Naive 
Random oversampling, precision and recall for both classes have increased slightly and the F1 score for low risk is higher. 
According to the low precision and recall, this model does not perform well, but compared to the Naive Random Forest works slightly better. The model's accuracy is low.


3- As shown in the following table,






<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Undersampling.PNG" width="700" height="600"  />




The metrics for the majority class are as follows:
- Precision: 1
- Recall: 0.40
- F1 Score: 0.57
- Model's Accuracy: 0.41
- Balanced Accuracy Score: 0.54

The metrics of the low risk class precision , recall and F1 score do not show a good performance. The model's accuracy and the balanced accuracy score are very low. Therefore this model is not a good classifier for both the majority and minority class.   








4- As shown in the following table,



<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Combine-sampling.PNG" width="700" height="600" />




The metrics for the majority class are as follows:
- Precision: 1
- Recall: 0.57
- F1 Score: 0.73
- Model's Accuracy: 0.57
- Balanced Accuracy Score: 0.68

The metrics of the majority class do not show a good performance. In fact, after combining the under and over sampling, we are not able to show a desireable performance at least for the majority class.


## Use Ensemble Classifiers to Predict Credit Risk

1- As shown in the following table,





<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Balanced-Random-Forest.PNG" width="700" height="600"  />


The metrics for the majority class are as follows:
- Precision: 1
- Recall: 0.87
- F1 Score: 0.93
- Model's Accuracy: 0.94
- Balanced Accuracy Score: 0.93

In fact, by choosing the balanced random forest classifier, we observe significient changes in the metric specially the last two. Therefore, this classifier will perform well if it is selected to predict the credit risk and reduce bias.  



2-As shown in the following table,



<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Easy-Ensemble-AdaBoost.PNG" width="700" height="600"  />




The metrics for the majority class are as follows:
- Precision: 1
- Recall: 0.94
- F1 Score: 0.97
- Model's Accuracy: 0.94
- Balanced Accuracy Score: 0.93 

By observing the existing metrics and in comparion with the five previous models, it is concluded that this classifier would be the best model for prediction credit resk and has less bias.

## Summary
We first performed the strategy of oversampling uning Naive Random Forest to predict the credit risk. In fact instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced. The result is shown that precision ("pre" column), recall ("rec" column) and F1 score are low for the majority and the minority class. Then we applied for another oversampling approach (SMOTE) to increase the size of the minority and the metrics of the minority class (precision, recall, and F1 score) are slightly improved over those of random oversampling, although this model is not still a suitable classifier to predict data. 

Undersampling is another technique to address class imbalance. Undersampling identifies clusters of the majority class, then generates synthetic data points, called centroids, that are representative of the clusters. By using undersampling, the results are unimpressive, especially for predicting data. These results are worse than those from oversampling! While resampling can attempt to address imbalance, it does not guarantee better results. 

An approach to resampling is to combine aspects of both oversampling and undersampling. SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms in two-step process:

1- Oversample the minority class with SMOTE.

2- Clean the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.

Resampling with SMOTEENN did not work miracles, but some of the metrics show an improvement over undersampling.

Lastly, we applied two ensemble learners to determine which algorithm results has the best performance. We trained a Balanced Random Forest Classifier and an Easy Ensemble AdaBoost classifier. In the Balanced Random Forest Classifier, we droped some of the lower ranked features to improve the model. However, compared to previous models, there have been dramatic positive changes in metrics, but it still has the potential to get better. Therefore, we apply Easy Ensemble AdaBoost Classifier which has the stronger performance and we choose the last model for predicting the credit risk. The results of the last classifier seem to be closer to the actual values. 
