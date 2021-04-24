# Credit_Risk_Analysis

## Project Overview
All around the world, people borrow money to produce cars, homes,start bussinesses and persue education.
Loans are essential part of modern society and present an opportunity and challenge for bank and another 
lender institutions. On one hand, loans create revenue with the interest rate generated, on the other hand, there is a risk of not paying people and lenders may loose money. Banks rely on income, credite scores and people's assets to reduce the risk. By increasing the financial technologies and using machine learning, bank can analyze this risk. Machine learning can process data to receive a single decision. 

This analysis can be summarized in the following steps:
- Use Python and Scikit-learn to predict credit risk.
- Compare the strengths and weaknesses of machine learning models.
- Assess how well a model classsifies and predicts data.

In addition, we apply resampling skills as well as build on old skills. These skills are important because machine learning requires to think about all the peices of the data analytics puzzle at once.

In fact, machine learning requires to think about people's aspects to the puzzle too. After all, the best analysis is not worth much if the stakeholders do not understand. We dig into the technical details and the puzzle peices, to several machine learning models and evaluate them to predict credit risk, and being able to predict credit risk with machine learning algorithms can help banks and financial institutions predict anomalies, reduce risk cases, monitor portfolios, and provide recommendations on what to do in cases of fraud.


## Resources
Software:[Python 3.7.6](https://www.python.org/downloads/) and [Jupyter Notebook](https://www.anaconda.com/products/individual)
- library: Scikit-learn


## Results
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Lastly, we’ll evaluate the performance of these models to be used to predict credit risk.

## Use Resampling Models to Predict Credit Risk
### Naive Random Oversampling






<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Naive-Random-Oversampling.PNG" width="700" height="600"/>







###  SMOTE Oversampling






<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/SMOTE-Oversampling.PNG" width="700" height="600"/>







### Undersampling







<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Undersampling.PNG" width="700" height="600"  />












## Use the SMOTEENN Algorithm to Predict Credit Risk
### Combination (Over and Under) Sampling




<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Combine-sampling.PNG" width="700" height="600" />





## Use Ensemble Classifiers to Predict Credit Risk
### Balanced Random Forest Classifier




<img src="" width="700" height="600"  />





### Balanced Random Forest Classifier




<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Balanced-Random-Forest.PNG" width="700" height="600"  />





### Easy Ensemble AdaBoost Classifier




<img src="https://github.com/halmasieh/Credit_Risk_Analysis/blob/main/Easy-Ensemble-AdaBoost.PNG" width="700" height="600"  />





## Summary
According to the observed percentages attributed to 5-star Vine reviews versus 5-star un-Vine reviews, it can be stated that
since the percentage of Vine reviews gave 5-star ratings is higher than un-Vine reviews, so, we could probably tell that the Vine
program has a positive bias. In order to support the statement of the positive bias that Vine reviews made versus the un-Vine reviews, 
we can state that from the view of sentimental reviews, people who are getting paid for Vine-reviews are more positive than the people who do not pay.

