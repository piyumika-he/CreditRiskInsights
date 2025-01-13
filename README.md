# Credit Risk Analysis and Visualization

This project focuses on Credit Risk Analysis by leveraging both machine learning and deep learning techniques to predict the likelihood of loan default. This is developed as part of a group project during my Bachelor’s degree in 2020. The project focuses on analyzing and visualizing credit risk data to identify patterns and insights that can assist in risk assessment.


## Problem
It is very important to identify whether the customer is risky or not before 
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

## Preprocessing
To ensure the models perform optimally, the following preprocessing steps were implemented:

Handling Missing Values: Missing data was replaced using statistical imputation techniques.
Feature Scaling: Applied normalization to bring all features to the same scale.
Class Balancing: Used SMOTE (Synthetic Minority Oversampling Technique) to handle the class imbalance in the dataset.
Feature Selection: Selected the most relevant features to reduce noise.


## Machine Learning Models
The following machine learning algorithms were implemented and evaluated:

Random Forest Classifier
Linear Discriminant Analysis (LDA)
K-Nearest Neighbors (KNN)
Ridge Regression
AdaBoost
Bagging
The models were evaluated using metrics such as accuracy, precision, recall, and F1-score. Among these, the Random Forest Classifier performed the best, achieving an accuracy of 78%.

## Deep Learning Model
A Feedforward Neural Network (FNN) was developed to further improve predictions. The architecture consists of multiple dense layers, dropout layers, and batch normalization to enhance generalization and stability.

Model Architecture:

Input Layer: Accepts features after preprocessing (scaled and balanced).
Hidden Layers:
Layer 1: 128 neurons, ReLU activation, L2 regularization, and batch normalization.
Layer 2: 64 neurons, ReLU activation, and batch normalization.
Layer 3: 32 neurons, ReLU activation, and dropout for regularization.
Output Layer: A single neuron with sigmoid activation for binary classification.
Loss Function: Binary Cross-Entropy Loss.
Optimizer: Adam with a learning rate of 0.0005.
The deep learning model achieved an accuracy of 71.3%, and further tuning is ongoing to bridge the performance gap with the Random Forest Classifier.

<img width="333" alt="image" src="https://github.com/user-attachments/assets/d2a51be6-e851-43b1-bd8e-dede553b1f49" />


## Technologies and Libraries Used
This project utilizes the following technologies and Python libraries:

### Data Analysis and Preprocessing:
Pandas
NumPy
Scikit-learn
Imbalanced-learn

### Machine Learning:
Scikit-learn

### Deep Learning:
TensorFlow
Keras

### Visualization:
Matplotlib
Seaborn

## Important Results
There are many low credit risk customers in the dataset. 

<img width="244" alt="image" src="https://github.com/user-attachments/assets/c5ac5971-18b0-4496-a4b6-ef1c64393686" />

Highest accuracy obtained with random forest model. - 78%

Consider the accuracy with comparison to the ROC curves. And the highest AUC value is 
taken the random forest and LDA techniques. 

<img width="445" alt="image" src="https://github.com/user-attachments/assets/eb7c7882-1cbc-4a4b-9d46-1fc1ff23ec57" />

## Future Improvements
Optimize the deep learning model with advanced architectures (e.g., convolutional or recurrent layers).
Use hyperparameter tuning tools like GridSearchCV.


