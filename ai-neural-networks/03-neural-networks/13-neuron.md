# Lesson 13 — The Artificial Neuron

A neuron combines input values, weights, and bias.

## Inputs and weights

Inputs: `x=[x1,x2,...,xn]`

Weights: `w=[w1,w2,...,wn]`

Each weight controls the contribution of its corresponding input. Bias is an extra learned number that shifts the weighted sum.

## Formula

`z = w1*x1 + w2*x2 + ... + wn*xn + b`

Then:

`a = activation(z)`

z is the pre-activation; a is the output after activation.

## Worked example

Inputs x1=2, x2=3; weights w1=0.5, w2=-1; bias b=2.

`z=0.5*2 + (-1)*3 + 2`

`z=1-3+2=0`

ReLU activation:

`ReLU(z)=max(0,z)`

Output=0.

## Why weights are learned

Weights may start at random values. Training estimates how loss changes with each parameter and adjusts them.

The neuron is not thinking; it is performing arithmetic.

## Practice

x1=4, x2=1; w1=2, w2=3; b=-2. Find z.

Answer: `2*4+3*1-2=9`
