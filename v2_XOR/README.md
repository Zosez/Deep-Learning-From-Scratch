# XOR Neural Network from Scratch

A complete implementation of a feedforward neural network using **only NumPy** to solve the classic **XOR (Exclusive OR)** problem. This project focuses on understanding the mathematics behind neural networks by implementing every component manually without relying on deep learning frameworks such as TensorFlow or PyTorch.

This project is part of my **Deep Learning From Scratch** learning journey.

---

## Why XOR?

The XOR problem is one of the most important problems in neural network history.

Unlike linear classification problems, XOR is **not linearly separable**, meaning a single-layer perceptron cannot solve it. By introducing a hidden layer and nonlinear activation functions, the neural network learns a nonlinear decision boundary capable of correctly classifying the XOR outputs.

| Input 1 | Input 2 | Output |
|---------:|---------:|-------:|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

---

## Project Objectives

- Build a neural network completely from scratch
- Understand forward propagation
- Implement backpropagation manually
- Learn gradient descent optimization
- Understand why hidden layers are necessary
- Visualize the learning process using the loss curve

---

## Features

- Feedforward Neural Network
- Multiple Hidden Neurons
- ReLU Activation Function
- Sigmoid Output Activation
- Binary Cross Entropy Loss
- Backpropagation from Scratch
- Gradient Descent Optimization
- Configurable Learning Rate
- Configurable Number of Epochs
- Loss Curve Visualization
- Prediction Function

---

## Technologies Used

- Python
- NumPy
- Matplotlib

---

## Project Structure

```
xor-neural-network/
│
├── neural_network.py      # Neural Network implementation
├── main.py                # Model training
├── README.md
```

---

## Neural Network Architecture

```
Input Layer (2 Neurons)
        │
        ▼
Hidden Layer (Configurable)
        │
      ReLU
        │
        ▼
Output Layer (1 Neuron)
        │
     Sigmoid
        │
        ▼
Binary Prediction
```

---

## Training Process

The network learns using the following pipeline:

1. Initialize weights and biases
2. Forward propagation
3. Compute Binary Cross Entropy loss
4. Perform backpropagation
5. Update weights using Gradient Descent
6. Repeat for multiple epochs

---

## Concepts Implemented

- Matrix Multiplication
- Weight Initialization
- Bias Initialization
- ReLU Activation
- Sigmoid Activation
- Binary Cross Entropy
- Forward Propagation
- Backpropagation
- Gradient Descent
- Binary Classification

---

## Sample Output

```
Epoch 1000 | Loss: 0.4312
Epoch 2000 | Loss: 0.1874
Epoch 3000 | Loss: 0.0621
...
```

Predictions:

```
Input    Prediction

[0,0] -> 0
[0,1] -> 1
[1,0] -> 1
[1,1] -> 0
```

---

## What I Learned

Through this project I gained a deeper understanding of:

- Why linear models fail on XOR
- The importance of hidden layers
- Nonlinear activation functions
- How gradients are computed using the chain rule
- How weights are updated during training
- The complete training pipeline of a neural network

---

## Future Improvements

- Configurable activation functions
- Multiple hidden layers
- Softmax output layer
- Mini-batch Gradient Descent
- He/Xavier Weight Initialization
- MNIST Digit Recognition
- Convolutional Neural Networks (CNNs)

---

## Learning Roadmap

- ✅ Neural Network for Binary Classification
- ✅ XOR Neural Network
- ⏳ Multi-Layer Neural Network
- ⏳ MNIST from Scratch
- ⏳ Softmax Classifier
- ⏳ CNN from Scratch
- ⏳ RNN from Scratch
- ⏳ Transformer from Scratch

---

## License

This project is created for educational purposes as part of my **Deep Learning From Scratch** repository.