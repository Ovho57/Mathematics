# Lesson 15 — Layers and Network Architecture

A neural network connects neurons in stages called layers.

## Input layer

Receives features. An image of 28x28 pixels can be flattened into 784 numbers.

## Hidden layers

Transform the information. A layer may have 32, 64, or more neurons. “Hidden” means between input and output.

## Output layer

Produces the prediction:
- one number for regression,
- one probability for binary classification,
- class scores or probabilities for multi-class classification.

## Example architecture

Input: 3 values
→ Dense layer: 4 neurons
→ ReLU
→ Dense layer: 2 neurons
→ Softmax
→ 2 class probabilities

## Dense layer

Each neuron receives every value from the previous layer.

`z = W*x + b`

`a = activation(z)`

## Parameter count

For n inputs and m neurons:
- weights = n*m
- biases = m
- total = n*m + m = m*(n+1)

Example: 3 inputs, 4 neurons:

`3*4 + 4 = 16 parameters`

## Why multiple layers?

Layers can build increasingly useful representations. Early layers may learn simple patterns; later layers combine them. More layers do not automatically mean better results.

## Practice

1. A dense layer has 5 inputs and 8 neurons. Number of weights and biases?
2. Total parameters?
3. What does output layer do?

Answer: 40 weights, 8 biases, 48 total; it produces the model's output.
