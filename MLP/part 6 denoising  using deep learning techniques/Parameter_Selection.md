# Parameter Selection

1. **input Layer**
## shape

- The input layer is designed to match the size of the images in the dataset (28x28 pixels).
- The 28x28 configuration ensures that each pixel in the image corresponds to a separate input node in the neural network.

2. **Encoder**
## Dense Layer

- The encoder consists of a dense layer with 128 neurons.
- The choice of 128 neurons in the dense layer represents a balance between capturing sufficient high-level features and maintaining computational efficiency.

## Activation Function - 'ReLU'

- Rectified Linear Unit (ReLU) is chosen as the activation function for the encoder.
- ReLU introduces non-linearity, allowing the network to learn complex relationships in the data.
- It is computationally efficient and helps mitigate the vanishing gradient problem.
3. **Decoder**
## Dense Layer

- The decoder mirrors the architecture of the encoder, featuring a dense layer with 28x28 neurons.
- The symmetric structure ensures that the autoencoder can effectively reconstruct the original image.
## Activation Function - 'Sigmoid'

- The sigmoid activation function is used in the decoder layer.
- Sigmoid squashes the output values between 0 and 1, which is suitable for binary classification tasks, such as pixel-wise image reconstruction.
- It is particularly effective in the context of denoising autoencoders as it models the probability of each pixel being part of the denoised image.
