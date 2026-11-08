# Lesson 5 — Vectors

A vector is an ordered list of numbers. It can represent measurements, coordinates, or the features of one example.

## 1. A vector

`x = [2, 5, 1]`

This vector has three components:
- x_1 = 2
- x_2 = 5
- x_3 = 1

Order matters. `[2,5,1]` is different from `[5,2,1]`.

## 2. Vector addition

Add corresponding components:

`[1,2] + [3,4] = [1+3, 2+4] = [4,6]`

Vectors must have the same length for this operation.

## 3. Scalar multiplication

A scalar is an ordinary number.

`3*[2,4] = [3*2, 3*4] = [6,12]`

## 4. Dot product

The dot product multiplies matching components and adds the results.

For:

`a=[2,3]`
`b=[4,5]`

`a dot b = 2*4 + 3*5 = 8 + 15 = 23`

This is a fundamental neural-network calculation.

## 5. Feature vectors

Suppose a house is described by:
- size = 120
- bedrooms = 3
- age = 10

We can represent it as:

`x=[120,3,10]`

A machine-learning model receives numerical features like these.

## 6. Vector length

The length (magnitude) of a vector is:

`||x|| = sqrt(x_1^2 + x_2^2 + ... + x_n^2)`

For `x=[3,4]`:

`||x|| = sqrt(3^2 + 4^2) = sqrt(9+16) = sqrt(25)=5`

## Practice

1. Add [2,1] and [5,7].
2. Multiply [3,4] by 2.
3. Find the dot product of [1,3] and [4,2].
4. Find the length of [6,8].

## Answers

1. [7,8]
2. [6,8]
3. 10
4. 10
