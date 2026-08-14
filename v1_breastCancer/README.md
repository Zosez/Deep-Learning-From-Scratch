# 🧠 Breast Cancer Classification Neural Network (From Scratch)

A fully connected Neural Network implemented **from scratch using only NumPy** to classify breast cancer tumors as **Malignant** or **Benign**.

This project is part of my **Deep Learning From Scratch** journey, where I implement core deep learning algorithms without using TensorFlow or PyTorch to understand the mathematics behind neural networks.

---

## 📌 Project Overview

The model is trained on the **Breast Cancer Wisconsin Dataset** from Scikit-learn.

Instead of relying on deep learning libraries, every component of the network is manually implemented, including:

- Forward Propagation
- Backpropagation
- Gradient Descent
- Weight Initialization
- Binary Cross Entropy Loss
- ReLU Activation
- Sigmoid Output Activation
- Prediction Pipeline

---

## 🏗️ Network Architecture

```
Input Layer (30 Features)
        │
        ▼
Hidden Layer (15 Neurons)
        │
      ReLU
        │
        ▼
Output Layer (1 Neuron)
        │
    Sigmoid
        │
        ▼
Binary Classification
```

---

## 🚀 Features

- Neural Network built entirely with NumPy
- No machine learning framework used
- Manual implementation of:
  - Feed Forward
  - Backpropagation
  - Gradient Descent
- Binary Cross Entropy loss
- Loss visualization using Matplotlib
- Predict function for unseen data

---

## 📂 Dataset

Dataset used:

- **Breast Cancer Wisconsin Diagnostic Dataset**
- Available directly from Scikit-learn

Features:
- 30 numerical features
- Binary Classification
  - `0` → Malignant
  - `1` → Benign

---

## 🛠 Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn (Dataset & preprocessing only)

> **Note:** Scikit-learn is only used to load the dataset and perform train-test splitting/scaling. The neural network itself is implemented completely from scratch.

---

## 📈 Training Process

1. Load dataset
2. Split into train and test sets
3. Normalize features
4. Initialize weights randomly
5. Forward propagation
6. Compute Binary Cross Entropy loss
7. Backpropagation
8. Update weights using Gradient Descent
9. Repeat for multiple epochs
10. Evaluate on test data

---

## 📊 Results

The model successfully learns to classify breast cancer tumors with high accuracy after training.

Example output:

```
Loss: ...
Accuracy: ~93%
```

*(Results may vary because of random weight initialization.)*

---

## 📚 Concepts Learned

This project helped reinforce understanding of:

- Artificial Neural Networks
- Matrix Multiplication
- Forward Propagation
- Backpropagation
- Chain Rule
- Gradient Descent
- ReLU Activation
- Sigmoid Function
- Binary Cross Entropy
- Weight Updates
- Binary Classification

---

## 📁 Project Structure

```
Breast-Cancer-Neural-Network/
│
├── Breast_Cancer_NN.ipynb
├── README.md
└── images/           # (Optional for plots)
```

---

## 🎯 Future Improvements

- Multiple hidden layers
- Different activation functions
- Adam Optimizer
- Mini-batch Gradient Descent
- L2 Regularization
- Dropout
- Model saving/loading
- Multi-class classification support

---

## 📖 Part of My Deep Learning Journey

This project is one milestone in my **Deep Learning From Scratch** repository.

Planned projects include:

- ✅ Neural Network for Breast Cancer Classification
- ⏳ XOR Neural Network
- ⏳ MNIST Digit Recognition (NumPy only)
- ⏳ Multi-layer Neural Networks
- ⏳ CNN From Scratch
- ⏳ RNN From Scratch
- ⏳ Transition to TensorFlow & PyTorch

---

## 👨‍💻 Author

**Kashyap Adhikari**

Aspiring AI Engineer passionate about understanding deep learning from first principles before using high-level frameworks.