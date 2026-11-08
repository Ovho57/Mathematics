# Lesson 24 — Build a Tiny Neural Network with Python and NumPy

This lesson builds a small network for a simple binary classification task. It is educational code, not a production-ready model.

## 1. Install NumPy

In a terminal:

`python -m pip install numpy`

## 2. A small dataset

We will use XOR-like data:

- [0,0] → 0
- [0,1] → 1
- [1,0] → 1
- [1,1] → 0

A single linear neuron cannot solve XOR. A hidden layer makes it possible.

## 3. Complete example

```python
import numpy as np

# Four input examples, two features each
X = np.array([
    [0, 0],
    [0, 1],
    [1, 0],
    [1, 1],
], dtype=float)

y = np.array([[0], [1], [1], [0]], dtype=float)

rng = np.random.default_rng(42)

# 2 input features -> 4 hidden neurons -> 1 output
W1 = rng.normal(0, 1, (2, 4))
b1 = np.zeros((1, 4))
W2 = rng.normal(0, 1, (4, 1))
b2 = np.zeros((1, 1))

def sigmoid(x):
    return 1 / (1 + np.exp(-x))

learning_rate = 0.5

for epoch in range(10000):
    # Forward propagation
    z1 = X @ W1 + b1
    a1 = np.tanh(z1)

    z2 = a1 @ W2 + b2
    prediction = sigmoid(z2)

    # Binary cross-entropy (numerically clipped)
    p = np.clip(prediction, 1e-8, 1 - 1e-8)
    loss = -np.mean(y * np.log(p) + (1-y) * np.log(1-p))

    # Backpropagation
    dz2 = (prediction - y) / len(X)
    dW2 = a1.T @ dz2
    db2 = np.sum(dz2, axis=0, keepdims=True)

    da1 = dz2 @ W2.T
    dz1 = da1 * (1 - a1**2)  # derivative of tanh
    dW1 = X.T @ dz1
    db1 = np.sum(dz1, axis=0, keepdims=True)

    # Gradient descent update
    W2 -= learning_rate * dW2
    b2 -= learning_rate * db2
    W1 -= learning_rate * dW1
    b1 -= learning_rate * db1

    if epoch % 1000 == 0:
        print(epoch, loss)

print("Predictions:")
print(sigmoid(np.tanh(X @ W1 + b1) @ W2 + b2))
```

## 4. Understand each part

- `X` stores inputs.
- `y` stores target answers.
- `W1`, `b1` are first-layer parameters.
- `W2`, `b2` are second-layer parameters.
- `@` means matrix multiplication in NumPy.
- `tanh` is the hidden activation.
- `sigmoid` converts output to a value between 0 and 1.
- Forward pass computes predictions.
- Backpropagation computes gradients.
- Gradient descent updates parameters.

## 5. Important

Training can vary with initialization and settings. The purpose is to inspect the math and code, not to guarantee a perfect result in every run.

## Challenges

1. Change hidden neurons from 4 to 8 (update dimensions).
2. Print loss every 100 epochs.
3. Try a smaller learning rate.
4. Explain why XOR needs a hidden layer for this model.
