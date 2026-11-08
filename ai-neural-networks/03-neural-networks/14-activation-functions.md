# Lesson 14 — Activation Functions

An activation function transforms a neuron's weighted sum.

Without nonlinear activations, stacking linear layers still results in a linear transformation. Nonlinear activations allow networks to represent more complex relationships.

## ReLU

`ReLU(x)=max(0,x)`

- ReLU(5)=5
- ReLU(-3)=0
- ReLU(0)=0

## Sigmoid

`sigmoid(x)=1/(1+exp(-x))`

Its output is between 0 and 1. It is often used for binary classification probabilities.

Approximate values:
- sigmoid(0)=0.5
- sigmoid(2)=0.88
- sigmoid(-2)=0.12

## Tanh

Tanh outputs between -1 and 1 and is centered around zero.

## Softmax

`softmax(z_i)=exp(z_i)/sum_j exp(z_j)`

Softmax converts scores into nonnegative values that sum to 1. It is commonly used for multi-class predictions.

## Common choices

- Hidden layers: ReLU or variants such as GELU.
- Binary classification output: sigmoid.
- Multi-class output: softmax.
- Regression: often a linear output.

## Practice

1. ReLU(-8)?
2. ReLU(3)?
3. What is sigmoid's range?
4. Why are nonlinear activations useful?

Answers: 0; 3; between 0 and 1; they let the network learn nonlinear patterns.
