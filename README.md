# 02 — PyTorch

After implementing neural networks from scratch, this section introduces **PyTorch**, a modern deep learning framework used to build, train, and deploy neural networks more efficiently.

The focus here is on learning how the concepts implemented manually in Section 01 are handled using a professional deep learning framework.

## 🎯 Goals

* Learn PyTorch fundamentals
* Understand tensors
* Work with automatic differentiation
* Build neural networks using `torch.nn`
* Create training loops
* Work with datasets and DataLoaders
* Train models using GPUs
* Understand optimizers
* Save and load trained models
* Build practical deep learning projects

## 📚 Topics Covered

### PyTorch Fundamentals

* Tensors
* Tensor operations
* Shapes and dimensions
* Broadcasting
* CPU vs GPU
* Device management

### Automatic Differentiation

* Computational graphs
* Gradients
* `requires_grad`
* `backward()`
* `torch.no_grad()`

### Neural Networks

* `nn.Module`
* Linear layers
* Activation functions
* Loss functions
* Sequential models

### Training

* Forward pass
* Loss calculation
* Backpropagation
* Optimizers
* Gradient zeroing
* Training and validation loops

### Data

* `Dataset`
* `DataLoader`
* Batching
* Shuffling
* Train/validation/test splits

## 🛠️ Technologies

* Python
* PyTorch
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook

## 📂 Projects

Projects in this section will gradually move from simple models to more realistic deep learning applications.

### Planned Projects

* [x] PyTorch tensor fundamentals
* [x] Linear regression
* [x] Binary classification
* [x] Neural network classifier
* [ ] MNIST classification
* [ ] Custom Dataset and DataLoader
* [x] GPU training
* [x] Model saving and loading
* [x] Hyperparameter experiments

## 🔄 From Scratch → PyTorch

The main objective is to connect the concepts from the previous section with PyTorch.

For example:

| From Scratch             | PyTorch                   |
| ------------------------ | ------------------------- |
| NumPy arrays             | Tensors                   |
| Manual gradients         | Autograd                  |
| Manual layers            | `nn.Module`               |
| Manual parameter updates | Optimizers                |
| Manual batching          | `DataLoader`              |
| Manual training loop     | PyTorch training pipeline |

This comparison helps me understand what the framework is doing behind the scenes rather than treating it as a black box.

## 🚀 Next Steps

After becoming comfortable with PyTorch, the journey moves into specialized areas of deep learning:

* Computer Vision
* Natural Language Processing

---

**Previous:** [`01-Deep-Learning-From-Scratch`](../01-Deep-Learning-From-Scratch/)

**Next:** [`03-Computer-Vision`](../03-Computer-Vision/)
