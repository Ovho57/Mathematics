# Lesson 17 — Backpropagation

Backpropagation efficiently calculates how the loss changes with each network parameter. It uses the chain rule from calculus.

## The main idea

A network makes a prediction during forward propagation. Backpropagation then works backward from the loss to determine which weights and biases contributed to the error and how they should change.

It does **not** itself update the weights. It calculates gradients. An optimizer such as gradient descent uses those gradients to update parameters.

## A tiny model

`z=w*x+b`

`prediction=z`

For a single example, use squared loss:

`L=(prediction-target)^2`

Suppose:
- x=2
- w=3
- b=1
- target=10

Forward pass:

`prediction=3*2+1=7`

Loss:

`L=(7-10)^2=9`

## Derivative of the loss

Since:

`L=(prediction-target)^2`

`dL/dprediction = 2*(prediction-target)`

At prediction=7 and target=10:

`dL/dprediction=2*(7-10)=-6`

Since prediction = w*x+b:

`dprediction/dw=x`

`dprediction/db=1`

Chain rule:

`dL/dw = dL/dprediction * dprediction/dw`

`dL/dw=-6*2=-12`

And:

`dL/db=-6*1=-6`

## Update the parameters

With learning rate 0.1:

`w_new = 3 - 0.1*(-12) = 4.2`

`b_new = 1 - 0.1*(-6) = 1.6`

The next prediction is:

`4.2*2+1.6=10`

For this simple example, the update reached the target exactly.

## Why it is called backward propagation

Forward: input → prediction → loss.

Backward: loss → output derivative → earlier layer derivatives → parameter gradients.

## Key distinction

- **Backpropagation:** calculates gradients.
- **Optimizer:** uses gradients to change parameters.
- **Training loop:** repeatedly performs forward pass, loss, backward pass, and update.

## Practice

If `L=(p-y)^2`, find `dL/dp`.

Answer: `2*(p-y)`.
