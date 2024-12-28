# Credit Risk Analysis and Visualization

This repository contains two Jupyter notebooks developed as part of a group project during my Bachelor’s degree in 2020. The project focuses on analyzing and visualizing credit risk data to identify patterns and insights that can assist in risk assessment.

## Features
Data Analysis: Exploratory data analysis to identify key trends and relationships.
Machine Learning Models: Implementation of classification algorithms tailored for credit risk prediction.
Visualization: Intuitive graphs for better understanding and communication of results.

## Introduction
Banks play an important role in the modern society which highly associated with money and the finance. Not 
like in the past most of people tends to deposit their money in banks due to the various reasons. Safety, higher 
saving interest rates are some of them. Apart from those facts bank loans are the most famous service among 
all the services which provided by banks. Land loans, house loans, Jewelry mortgage loans are the frequently 
issued loan types. In most countries, bank loans are the main source of financing for small and medium sized 
enterprises. But issuing a loan to a customer is not just an easy task. It is very important to identify whether the 
customer is risky or not. So usually bank authorities analyze previous records (transactions and payments) to 
determine the customers’ nature. 

## Problem
As explained in the introduction It is very important to identify whether the customer is risky or not before 
issuing a bank loan. Models make it possible to identify relationships between variables and to understand how 
variables, working on their own and together, influence an overall system. So we tried to develop a model to predict 
whether a customer is in a high credit risk (risky) or low credit risk (non risky). 

## Dataset
  There were two datasets. 
  Customer data: -1125 observations 
  Payment data: - 8250 observations 
  Source: - https://www.kaggle.com/praveengovi/credit-risk-classification-dataset 
  dropped the fea 6 & fea 11 due to the lack of the information. 
  dropped the update date, Report Date, Prod code and Product limit due to the higher amount of 
missing values and we are not going to do a time series analysis. 
  grouped payment data by “id” variable and then combine two data sets. 
  Now combined data set has 1125 observations and 18 variables. 

Handling Data Imbalance
Given the imbalance in the sizes of the positive and negative samples in the dataset, oversampling techniques such as SMOTE (Synthetic Minority Oversampling Technique) were used to balance the dataset. This ensures that the machine learning models are not biased toward the majority class and can perform effectively across all classes.

## Important Results
There are many low credit risk customers in the dataset. 
<img width="244" alt="image" src="https://github.com/user-attachments/assets/c5ac5971-18b0-4496-a4b6-ef1c64393686" />

Highest accuracy obtained with random forest model. - 78%

Consider the accuracy with comparison to the ROC curves. And the highest AUC value is 
taken the random forest and LDA techniques. 
<img width="445" alt="image" src="https://github.com/user-attachments/assets/eb7c7882-1cbc-4a4b-9d46-1fc1ff23ec57" />


