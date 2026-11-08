# Lesson 16 — Forward Propagation

Forward propagation sends inputs through a network to calculate a prediction.

## One neuron

`z=w*x+b`

`a=activation(z)`

## One layer

For many neurons:

`z=W*x+b`

`a=activation(z)`

## Two-layer example

Input:

`x=[1,2]`

First layer weights:

`W1=[[1,1],[2,-1]]`

Bias:

`b1=[0,1]`

First neuron:

`1*1+1*2+0=3`

Second neuron:

`2*1+(-1)*2+1=1`

Thus:

`z1=[3,1]`

Apply ReLU:

`a1=[3,1]`

Second layer weights:

`W2=[[2,-1]]`

Bias b2=0:

`z2=2*3+(-1)*1=5`

The output is 5 if the output activation is linear.

## Why forward?

Values flow from input toward output:

Input → layer 1 → layer 2 → prediction.

Training later sends gradient information backward.

## Practice

Input x=[2,1], weights [3,4], bias=-1. Calculate the pre-activation.

Answer: `3*2+4*1-1=9`
