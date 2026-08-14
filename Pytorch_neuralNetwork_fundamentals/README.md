# PyTorch Neural Network Fundamentals

This project contains a beginner-friendly PyTorch notebook that demonstrates how to build and train a simple neural network for binary classification on a circular dataset.

## Notebook

- `torch_nn_fundamentals.ipynb`

## What this notebook covers

- Creating synthetic classification data using `sklearn.datasets.make_circles`
- Converting NumPy arrays into PyTorch tensors
- Splitting data into training and test sets
- Building a neural network with `torch.nn`
- Setting up a loss function and optimizer
- Training a model with a manual training loop
- Evaluating performance and checking accuracy
- Visualizing decision boundaries
- Improving model architecture with extra layers and ReLU activations

## Key concepts learned

- Input and output shapes
- Binary classification with `BCEWithLogitsLoss`
- Sigmoid activation for binary outputs
- `torch.nn.Linear` layers
- Forward pass and backpropagation
- Gradient descent via optimizer steps
- Training vs. testing behavior

## Requirements

Install the following Python packages:

```bash
pip install torch numpy pandas scikit-learn matplotlib
```

## Recommended setup

Use a Python environment with Jupyter support:

```bash
pip install notebook jupyterlab
```

## How to run

1. Open the notebook in Jupyter or VS Code.
2. Run the cells in order from top to bottom.
3. Observe the model training progress and the final decision boundary plots.

## Project structure

```text
Pytorch_neuralNetwork_fundamentals/
├── README.md
└── torch_nn_fundamentals.ipynb
```

## Notes

This notebook is designed as a learning example and focuses on practical understanding rather than production-level training code. It is a good starting point for learning how neural networks work in PyTorch.
