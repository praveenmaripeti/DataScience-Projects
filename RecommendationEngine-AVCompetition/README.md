# Overview & Approach to Solution
This hackathon hosted on Analytics Vidhya involves predicting the number of attempts for a successful submission to online programming challenges. Data of programmers and questions they solved previously were given along with the time they took to solve the questions. 

## EDA
In this notebook, I performed exploratory analysis of the features and target variables. It consists of studying the correlation between variables, participation from various countries, number of participants at varying skill levels. I tried to make sense of variables such as problem level which are represented by alphabets A - H.

![screenshot](https://user-images.githubusercontent.com/58431708/100081285-d92eca00-2e6c-11eb-9b92-a98adb877edb.jpg)

## Feature Engineering
The given features had null values and several tags in string format in one column. I created separate column for each tag and encoded country and rank variables. The raw data contained null values in about 25% of rows. As removing them would cause loss of valuable data, I used sklearn's iterative imputer to impute the missing values.

## Modeling
In the early stage of modeling, I realized that non-linear classifiers such as random forest are doing a better job than linear classifiers on this dataset. Therefore I used only non-linear classifiers to try out different models. I started with a simple random classifier with default params. The evaluation metric is chosen to be F1 weighted as the same metric is used in the competition. To improve upon the performance of simple random forest classifier, I used randomized search cross validation over a range of parameters and it did result in a slightly improved classification. Following this, I implemented a Extreme Gradient Boosting Classifier (XGBoost) after tuning the hyperparameters and it resulted in a significant improvement in F1 score over the first two models. Lastly, I used stacking classifier which used parameter tuned XGBoost classifier and Random Forest Classifier as base estimators and another XGBoost CLassifier with default parameters as final estimator. This however did not lead to a significant improvement in F1 score. I therefore selected the third model (XGBClassifier) for predicting on the test set. 

## Analytics Vidhya Hackathon Rank
My solution was ranked 35 out of 5469 participants as of Nov 24, 2020. Rank 1 F1 score is 0.51 and my F1 score is 0.482.

## View full solution on nbviewer with the following link
https://nbviewer.jupyter.org/github/praveenmaripeti/Data-Science-Projects/blob/main/RecommendationEngine-AVCompetition/recommendation-engine-av-hackathon.ipynb
