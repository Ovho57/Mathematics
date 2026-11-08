# Lesson 6 — Matrices and Matrix Multiplication

A matrix is a rectangular grid of numbers. Matrices allow neural networks to process many calculations together.

## 1. Matrix shape

Example:

`A = [[1,2,3],[4,5,6]]`

This matrix has 2 rows and 3 columns. Its shape is 2 by 3, written 2x3.

## 2. Matrix addition

Add corresponding entries:

`[[1,2],[3,4]] + [[5,6],[7,8]] = [[6,8],[10,12]]`

The matrices must have the same shape.

## 3. Matrix-vector multiplication

Let:

`A = [[1,2],[3,4]]`
`x = [5,6]`

First row:

`1*5 + 2*6 = 17`

Second row:

`3*5 + 4*6 = 39`

Therefore:

`A*x = [17,39]`

Each row of the matrix performs a dot product with the vector.

## 4. Dimensions matter

If A has shape m by n, and x has n components, then A*x produces m components.

Example:
- A: 3x2
- x: 2 components
- output: 3 components

The inner dimensions must match.

## 5. A layer in matrix form

Suppose a layer has 2 inputs and 3 neurons.

Weights:

`W = [[1,0],[0,2],[1,1]]`

Input:

`x=[3,4]`

Calculate:

- neuron 1: `1*3 + 0*4 = 3`
- neuron 2: `0*3 + 2*4 = 8`
- neuron 3: `1*3 + 1*4 = 7`

Output before bias/activation:

`W*x = [3,8,7]`

A whole layer is many weighted sums organized into a matrix operation.

## Practice

1. Find [[2,1],[0,3]] * [4,5].
2. What is the shape of a matrix with 4 rows and 7 columns?
3. A 5x3 matrix multiplies a 3-component vector. How many outputs result?

## Answers

1. [13,15]
2. 4x7
3. 5
