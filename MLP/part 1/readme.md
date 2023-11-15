# MLPMLP Classifier

This Python script demonstrates the use of a neural network classifier for predicting satisfaction based on input features. The code uses the scikit-learn library for building and training the neural network.

## Prerequisites

Make sure you have the required libraries installed. You can install them using the following:

```bash
pip install pandas scikit-learn matplotlib
```
# Description

## Data Preprocessing

- Drops unnecessary columns ('Unnamed: 0' and 'id') from both datasets.
- Encodes the target variable 'satisfaction' using LabelEncoder.

## Data Splitting

- Splits the training data into features (X) and the target variable (y).
- Splits the data into training and testing sets using train_test_split.

## Neural Network Initialization

- Initializes a Multilayer Perceptron (MLP) Classifier with two hidden layers, each having 100 and 50 neurons, respectively.
- Sets additional parameters, including the learning rate and solver type.
## Training Loss Plot

- Plots the training loss over iterations.

## Confusion Matrix Plot

- Plots the confusion matrix for model evaluation.

# Hyperparameters

You can experiment with the following hyperparameters to potentially improve model performance:

- Hidden layer sizes
- Learning rate
- Solver type
- Number of training iterations (max_iter)
 
# Licese
This code is licensed under the GNU License 