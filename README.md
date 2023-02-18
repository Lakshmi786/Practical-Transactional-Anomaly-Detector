# Transaction Anomaly Detector
This project is about detecting fraudulent transactions in the finance domain using an anomaly detection system. The aim is to develop an automated approach to identify these fraudulent transactions from a database containing millions of records.

## Table of Contents
#### Motivation
#### Anomaly Detection
#### Challenges
#### Machine Learning Approach
#### Dataset
#### Installation
#### Usage
#### Results


## Motivation
The purpose of this project is to provide an introduction to Anomaly Detection using Python. The guide covers the following topics:

What is Anomaly?
What are the challenges of Traditional methods to do Anomaly?
Using Isolation Forest for Anomaly Detection.
How to explain the results?

## Anomaly Detection
Anomaly refers to something that is unusual or different from what is expected. In the context of financial transactions, an anomaly could mean a transaction that is abnormal or outside the normal pattern of behavior. For example, if a customer's normal spending pattern is 500 dollars per month, a transaction of 5000 dollars would be considered an anomaly and warrant further investigation.

## Challenges
The main challenge with fraudulent transactions is the sheer size of the database. A manual validation of the data to identify anomalies is impossible. If the problem is that the human experts don't have the time to go through the dataset, we can try to automate their decision process.

One possible approach is a rule-based system, where experts compile a set of rules to single out fraudulent transactions. However, this approach has several problems:

Coming up with a good set of rules requires a lot of expertise and work.
If the dataset format changes or a different dataset is used with different distribution, the complete set of rules needs to be reworked to reflect the new situation.
It is impossible to predict all shapes and forms that anomalies can assume.

## Machine Learning Approach
To address the above problem of the unknown nature of fraudulent transactions, we can make use of the data we have in the database. We have to build a system that learns from the data what constitutes an anomaly.

The first step is to train an unsupervised model on our data to learn about the distribution of data and to get a sense of what an anomaly is in our context. In step two, we use this model to predict the likelihood of a transaction being fraudulent for every transaction using what it has learned in the above step.

A machine learning model will never give a definitive answer of whether a transaction is fraudulent. There will always be inherent uncertainty in the answers it gives us. If our model gives a continuous value as the anomaly score that reflects the model's certainty of the transaction likely to be an anomaly, we can choose ourselves how wide we want to cast our net while looking for possible anomalies.

The output of the model will be a mapping of every transaction to a certain anomaly score. This score reflects how certain our model is of a certain transaction as an anomaly or not. If we want to consider some subset of transaction we have to set a threshold. The nature of the anomaly will help us to consider how wider net we want to perform. The downside is we might not understand why a transaction is an anomaly. That's why we have explainability to the model to understand why the model has flagged a certain transaction as an anomaly.

## Data Exploration:

The dataset has 11 columns and over 6 million rows.

For the purpose of this project, we'll only be using a small subset of the data, due to the limitations of the Colab instance.

We'll look at the distribution of the class labels in the dataset.

We have a binary classification problem where the positive class represents a fraudulent transaction.

We'll look at the distribution of the classes in the dataset.

## Distribution of Class Labels:

In the following cells, we'll plot the distribution of the two class labels in the dataset.

The class distribution in the dataset is heavily imbalanced, with only a small percentage of the data representing fraudulent transactions. This is something we'll need to keep in mind when we build our models.

## Data Preparation:

In the following cells, we'll prepare the data for use with the Isolation Forest model.

We'll drop the columns that we won't be using, and then we'll encode the categorical variables.

After this, we'll perform the train-test split.

## Model Training:

In the following cells, we'll train the Isolation Forest model and evaluate its performance.

We'll use the following metrics to evaluate the model:

Precision
Recall
F1 Score
ROC AUC Score
Precision-Recall Curve
ROC Curve
We'll also use SHAP (SHapley Additive exPlanations) to explain the model's predictions.

SHAP is a game theoretic approach to explain the output of any machine learning model.

## Explainability of Model:

In the following cells, we'll use SHAP to explain the model's predictions.

We'll visualize the SHAP values for each of the features in the dataset, to see how much each feature contributes to the final prediction.

We'll also use the summary plot to get a global overview of the feature importance.

## Conclusion:

In this project, we've used the Isolation Forest algorithm to detect fraudulent transactions in a financial dataset.

We've shown how to prepare the data for use with the model, and how to evaluate its performance using various metrics.

We've also used SHAP to explain the model's predictions and visualize the feature importance.

This project serves as a good introduction to anomaly detection in Python, and provides a solid foundation for further exploration of the topic.
