# Optimal Number of Hidden Neurons

## Introduction

This document analyzes the impact of the number of hidden neurons on the Mean Squared Error (MSE) in a Multi-Layer Perceptron (MLP) regression model. The goal is to understand how adjusting the number of hidden neurons affects the model's performance.

## Code Overview

The code snippet below explores the relationship between the number of hidden neurons and the MSE for a linear function. The code uses an MLPRegressor from scikit-learn.

```python
# Additional plot: Mean Squared Error vs. Number of Hidden Neurons
hidden_neurons = [10, 20, 30, 40, 50, 60, 70, 90, 100, 120, 160]
mse_values = []

for neurons in hidden_neurons:
    mlp = MLPRegressor(hidden_layer_sizes=(200, neurons), max_iter=10000, random_state=42)
    mlp.fit(x_train_linear_2.reshape(-1, 1), y_train_linear_2)
    y_pred = mlp.predict(x_test.reshape(-1, 1))
    mse = mean_squared_error(y_test_linear, y_pred)
    mse_values.append(mse)

plt.figure(figsize=(8, 6))
plt.plot(hidden_neurons, mse_values, marker='o')
plt.title('Mean Squared Error vs. Number of Hidden Neurons')
plt.xlabel('Number of Hidden Neurons')
plt.ylabel('Mean Squared Error')
plt.show()
```

![MSE vs. Number of Hidden Neurons](C:\Users\reza\Documents\GitHub\MLP\output_balance.png)
# Analysis

- The plot visualizes the relationship between the number of hidden neurons and the resulting MSE. The x-axis represents the number of hidden neurons, and the y-axis represents the MSE.

# Conclusion

The plot suggests that adding more hidden neurons does not always lead to better performance. In this specific case, increasing the number of hidden neurons beyond a certain point (around 70 neurons) leads to a worsening of the MSE. This indicates that finding a balance between the number of neurons and layers is crucial for achieving optimal model performance.

Considerations for determining the optimal architecture include avoiding overfitting, optimizing training time, and achieving satisfactory generalization on unseen data. Experimentation and validation on different datasets may be required to find the most suitable model architecture.

By carefully selecting the number of hidden neurons and layers, practitioners can enhance the performance and efficiency of MLP models for regression tasks.