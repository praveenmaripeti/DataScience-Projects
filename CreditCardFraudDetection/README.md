# Project Overview
This project contains analysis of credit card transactions made by European cardholders in Septmber 2013. I also build a classifier to predict fradulent transactions. This dataset presents transactions that occurred in two days, where there are 492 frauds out of 284,807 transactions. The dataset is severely imbalanced, the positive cases (frauds) account for 0.172% of all transactions.

## Exploratory Analysis
In the analysis, I study the distribution of transactions amounts, class distribution, correlation between the features and target. 
![heatmap](https://user-images.githubusercontent.com/58431708/99896286-21a38780-2cb5-11eb-8081-000be0d9aefe.png)

## Addressing class imbalance issue
In this segment, I consider oversampling and undersmapling techniques to mitigate class imbalance issues. I choose ROC AUC curve as my metrics which is an appropriate metric for imabalanced data.

## Model
I implement Logistic Regression and Random Forest Classifiers and choose the latter to try out various approaches aimed at minimizing the classification error. I use confusion matrix to show how the samples are classified with undersampling, oversampling and undersampling+oversampling. Finally I will use the best performing model for predicting fradulent transactions.

![confusion matrix](https://user-images.githubusercontent.com/58431708/99896383-29aff700-2cb6-11eb-848b-c97b966c60e7.png)

