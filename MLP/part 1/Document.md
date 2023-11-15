# Multilayer Perceptron (MLP) Layers

The code utilizes scikit-learn's MLPClassifier to create a Multilayer Perceptron (MLP) for predicting satisfaction based on input features. The architecture of the neural network is defined by the hidden layers specified in the `hidden_layer_sizes` parameter. Let's break down the key aspects:

## Neural Network Architecture

The MLP in this code consists of two hidden layers:
- First Hidden Layer: 100 neurons
- Second Hidden Layer: 50 neurons

These hidden layers, along with the input and output layers, collectively form the architecture of the neural network. The `activation='relu'` parameter indicates the Rectified Linear Unit (ReLU) activation function is used in the hidden layers.

### Code Snippet
```python
# Initialize the neural network classifier
clf = MLPClassifier(hidden_layer_sizes=(100, 50), max_iter=500, activation='relu', random_state=42)
```

# Adam Optimization Algorithm

the Adam optimization algorithm is employed to train the neural network. Adam combines techniques from RMSprop and Momentum, providing an adaptive learning rate for each parameter during training. Here's a brief overview:

## Exponential Moving Average of Gradients (Momentum)

Maintains an exponentially decaying average of past gradients to keep track of the direction of the gradient.

## Exponential Moving Average of Squared Gradients (RMSprop)

Maintains an exponentially decaying average of the squared gradients to adapt the learning rates for each parameter individually.

## Bias Correction

Includes a bias correction term to handle the initialization bias of the moving averages.

# Algorithm Steps:

## Initialize parameters:

- Set the learning rate (α), decay rates for moment estimates (β1 and β2), and a small constant to prevent division by zero (ε).

## Initialize moment estimates:

- Initialize the first and second moments to zero.

## Iterative Update:

- For each iteration, calculate the gradient of the objective function with respect to the parameters.
- Update the first moment estimate (momentum) and the second moment estimate (squared gradients) using exponential decay.
- Correct the bias in the estimates.
- Update the parameters using the corrected estimates and the learning rate.


