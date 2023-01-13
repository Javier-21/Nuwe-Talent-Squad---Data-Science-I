# Nuwe Talent Squad Data Science I
## Introduction
This repository contains my solution to a problem proposed by *Nuwe*.

## Problem
The problem in to predict the state of the rockets based on the values of their sensors.

To create the solution I have two files:
- **space_X_train.csv**: It contains 2100 records and seven columns, six are the values of the different sensors and the other is the state of the rocket.
- **space_X_train.csv**: It contains 900 records with only the values of the six sensors to predict the state.

The rocket can have five different states:
- **0**: Stable
- **1**: Light turbulence
- **2**: Moderate turbulence
- **3**: Severe turbulence
- **4**: Extreme turbulence

## Solution
The first step was to perform the data exploration. The only relevant thing I found was that there was a high correlation between target and labels, but also between the labels and other labels.

Later, I standardized the labels and split the **space_X_train.csv** into two different dataset, one for training and one for testing.
With this split, the next step was to select the best model for the solution.
I tried a *Random forest*, a *Decision Tree*, a *Support Vector Machine*, a *Naive Bayes*,  an *XGBoost*, an *Artificila Neural Netowrk* (*ANN*).
The best results were obtained by *ANN*, created with the *Keras* library. This *ANN* contained four layer, the first three with 50 neurons and the output layer with 5 neurons.

Once I had the best model, I had to tune the hyperparameters to achieve the best results. With the grid search, I tried different values for the number of hidden layer neurons, the batch size, the number of epochs, and the weight initialization technique.

Operations indicated that the best parameter for *ANN* was to use 150 neurons in each hidden layer, a batch size of 16, perform 50 epochs, and do a normal initialization for the weight.

## Result

## License
- [*Javier Alegre Revuelta*](https://github.com/Javier-21)
