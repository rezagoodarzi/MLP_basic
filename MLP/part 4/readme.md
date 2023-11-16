# MLP Regression Model
This repository contains code for training a Multi-Layer Perceptron (MLP) regression model using the scikit-learn library.
The model is trained to predict a target variable based on input features.

# Introduction
The main objective of this code is to demonstrate the training and evaluation of an MLP regression model using scikit-learn.
The model is configured with varying hidden layer sizes, and the performance is evaluated using mean squared error (MSE). The code also includes functions for plotting actual vs predicted values and visualizing MSE across different hidden layer sizes.

# Function

## train_mlp_and_get_mse

This function trains an MLP regression model with the specified hidden layer sizes and returns the mean squared error (MSE) on the test set.

## plot_actual_vs_predicted

This function takes an MLP model and input data, then plots the actual vs predicted values. It includes the training set for comparison.

## plot_mse_vs_hidden_layers

This function plots the MSE for different hidden layer sizes.

## find_best_neurons_and_layers

This function iterates over a range of hidden layer sizes and identifies the configuration that yields the lowest MSE.

## plot_mse_vs_neurons

This function plots the MSE for different numbers of neurons with the best-hidden layer sizes.

# Challenges with Small Datasets

1. **Limited Generalization**

- Models trained on small datasets may struggle to generalize to new instances, resulting in poor performance on validation or test sets.

2. **Hyperparameter Sensitivity**

- Neural networks, including MLPs, often have several hyperparameters. With small datasets, the model's performance can be highly sensitive to these hyperparameters, making fine-tuning challenging.

Working with small datasets requires a thoughtful approach to prevent overfitting and improve model generalization.
Experiment with the strategies mentioned above, iterate on different configurations, and monitor the model's performance closely.
It may take some trial and error to find the optimal settings for your specific small dataset.
# Result

The best-hidden layer sizes and associated MSE are printed, and additional visualizations are provided to assess the model's performance.

# License

This code is licensed under the GNU License.


