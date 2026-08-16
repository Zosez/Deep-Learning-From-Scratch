# Handwritten Digit Classification with PyTorch

A handwritten digit classification project built using **PyTorch** and the `sklearn` digits dataset.

This project is part of my **Deep Learning Journey**, where I am progressing from implementing neural networks from scratch with NumPy to using modern deep learning frameworks such as PyTorch.

The main goal of this project is to understand the basic PyTorch workflow for building, training, evaluating, and saving a neural network.

---

## Project Overview

The model learns to classify handwritten digits from **0 to 9**.

The dataset used is the `load_digits()` dataset from Scikit-learn. Each image is an **8 × 8 grayscale image**, resulting in:

```text
8 × 8 = 64 input features
```

The model receives these 64 pixel values and predicts one of the 10 possible digit classes.

```text
8 × 8 Image
     ↓
64 Features
     ↓
Neural Network
     ↓
10 Output Classes
     ↓
Predicted Digit
```

---

## Dataset

This project uses:

```python
from sklearn.datasets import load_digits

digits = load_digits()
```

The dataset contains handwritten digit images representing the numbers **0–9**.

### Input

Each image has:

```text
8 × 8 pixels
```

and is represented as:

```text
64 features
```

### Output

The target is one of:

```text
0, 1, 2, 3, 4, 5, 6, 7, 8, 9
```

The dataset is divided into:

* **80% training data**
* **20% testing data**

---

## Technologies Used

* Python
* PyTorch
* NumPy
* Matplotlib
* Scikit-learn

---

## Neural Network Architecture

The model is implemented using PyTorch's `nn.Module`.

```text
Input Layer
64 neurons
    ↓
Linear Layer
64 → 128
    ↓
ReLU
    ↓
Linear Layer
128 → 128
    ↓
ReLU
    ↓
Output Layer
128 → 10
```

### Model

```python
class digitClassification(nn.Module):

    def __init__(self):
        super().__init__()

        self.layers = nn.Sequential(
            nn.Linear(in_features=64, out_features=128),
            nn.ReLU(),
            nn.Linear(in_features=128, out_features=128),
            nn.ReLU(),
            nn.Linear(in_features=128, out_features=10)
        )

    def forward(self, X):
        return self.layers(X)
```

---

## Training

The model is trained using:

### Loss Function

```python
nn.CrossEntropyLoss()
```

Cross Entropy is suitable for this problem because this is a **multi-class classification** task with 10 possible classes.

### Optimizer

```python
torch.optim.SGD()
```

with a learning rate of:

```text
0.03
```

### Training Configuration

```text
Epochs: 1000
Optimizer: SGD
Learning Rate: 0.03
Loss: Cross Entropy
```

---

## Training Process

The training loop follows the standard deep learning workflow:

```text
Input Data
    ↓
Forward Pass
    ↓
Calculate Loss
    ↓
Calculate Predictions
    ↓
Calculate Accuracy
    ↓
Zero Gradients
    ↓
Backpropagation
    ↓
Update Parameters
    ↓
Repeat
```

The model is evaluated on the test dataset periodically during training.

---

## Prediction

The model produces **logits** for each of the 10 classes.

For example:

```text
[1.2, -0.5, 0.8, ..., 4.7, ...]
```

Softmax can then convert the logits into probabilities:

```python
torch.softmax(logits, dim=-1)
```

The predicted class is obtained using:

```python
torch.argmax(predictions, dim=-1)
```

The class with the highest probability becomes the predicted digit.

---

## Evaluation

A custom accuracy function is used:

```python
def accuracy_fn(y_true, y_pred):
    correct = torch.eq(y_true, y_pred).sum().item()
    acc = (correct / len(y_pred)) * 100
    return acc
```

The model tracks:

* Training loss
* Training accuracy
* Testing loss
* Testing accuracy

The training and testing loss are also visualized using Matplotlib.

---

## Example Prediction

The trained model can be tested against individual handwritten digits from the dataset.

For example:

```text
Input Image: 8

Model Prediction: 8
```

and:

```text
Input Image: 4

Model Prediction: 4
```

This provides a simple way to verify that the trained model can recognize individual samples.

---

## Device Support

The notebook automatically checks whether CUDA is available:

```python
device = "cuda" if torch.cuda.is_available() else "cpu"
```

If a compatible GPU is available, the model and tensors are moved to the GPU.

Otherwise, the model runs on the CPU.

---

## Model Saving

After training, the model parameters are saved using PyTorch's `state_dict()`:

```python
torch.save(
    model1.state_dict(),
    "Hand_written_digits_classification.pth"
)
```

This allows the trained parameters to be reused later without retraining the model.

---

## Project Structure

```text
03-Handwritten-Digit-Classification/
│
├── hand_written_digit.ipynb
├── Hand_written_digits_classification.pth
└── README.md
```

---

## What I Learned

Through this project, I learned the basic workflow of building neural networks with PyTorch.

### PyTorch Fundamentals

* `torch.Tensor`
* `nn.Module`
* `nn.Sequential`
* `nn.Linear`
* `nn.ReLU`
* `nn.CrossEntropyLoss`
* `torch.optim.SGD`
* `model.train()`
* `model.eval()`
* `torch.inference_mode()`
* `state_dict()`

### Deep Learning Concepts

* Multi-class classification
* Logits
* Softmax
* Cross Entropy Loss
* Backpropagation
* Gradient Descent
* Training vs testing
* Model evaluation
* GPU/CPU computation

---

## From Scratch vs PyTorch

This project represents an important step in my learning progression.

Previously, I implemented neural networks manually using NumPy, including:

```text
Forward Propagation
        ↓
Loss Calculation
        ↓
Backpropagation
        ↓
Gradient Descent
        ↓
Weight Updates
```

In this project, PyTorch handles much of the underlying mathematical computation through **autograd** and its neural network and optimization APIs.

The purpose is not just to make the model work faster, but to understand how the concepts I implemented from scratch translate into a modern deep learning framework.

---

## Learning Progression

```text
Neural Network From Scratch
        ↓
Breast Cancer Classification
        ↓
XOR Neural Network
        ↓
        ┌──────────────────────┐
        │ PyTorch              │
        │                      │
        │ Handwritten Digits   │
        └──────────────────────┘
        ↓
CNN
        ↓
Computer Vision
        ↓
RNN / LSTM
        ↓
Transformers
```

---

## Future Improvements

Possible extensions for this project include:

* Normalize the input features
* Experiment with different network architectures
* Compare SGD with Adam
* Experiment with learning rates
* Add a confusion matrix
* Add a classification report
* Test on more unseen examples
* Experiment with the actual MNIST dataset
* Build a CNN for digit classification

---

## Conclusion

This project marks my transition from **building neural networks from scratch** to using **PyTorch** to build and train neural networks.

The main focus was understanding the complete PyTorch workflow:

```text
Dataset
   ↓
Preprocessing
   ↓
Model
   ↓
Loss Function
   ↓
Optimizer
   ↓
Training Loop
   ↓
Evaluation
   ↓
Prediction
   ↓
Model Saving
```

This project serves as the foundation for the next stage of my deep learning journey, where I will move toward **Convolutional Neural Networks and Computer Vision**.

---

## License

This project is created for educational purposes as part of my **Deep Learning Journey**.
