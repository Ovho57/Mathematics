# Lesson 1 — Numbers, Arithmetic, and Order of Operations

Neural networks repeatedly add, multiply, subtract, and divide numbers. Arithmetic is the foundation.

## 1. The four basic operations

### Addition

Addition combines quantities.

Example:
`7 + 5 = 12`

### Subtraction

Subtraction finds a difference.

Example:
`12 - 5 = 7`

### Multiplication

Multiplication is repeated addition.

`4 * 3 = 4 + 4 + 4 = 12`

In AI, multiplication is especially common. A model multiplies inputs by weights.

### Division

Division splits a quantity into equal parts.

`12 / 3 = 4`

## 2. Negative numbers

Numbers below zero are negative.

Examples:
- `-3 + 5 = 2`
- `4 - 9 = -5`
- `(-2) * 3 = -6`
- `(-2) * (-3) = 6`

Multiplication sign rules:
- positive * positive = positive
- positive * negative = negative
- negative * positive = negative
- negative * negative = positive

## 3. Fractions and decimals

A fraction represents division.

`3/4 = 0.75`

To add fractions with the same denominator:

`2/5 + 1/5 = 3/5`

For different denominators, find a common denominator:

`1/2 + 1/4 = 2/4 + 1/4 = 3/4`

Decimals are often used to represent weights and probabilities:
- `0.5` means one half.
- `0.25` means one quarter.
- `0.01` means one hundredth.

## 4. Order of operations

Use this order:
1. Parentheses
2. Exponents
3. Multiplication and division, left to right
4. Addition and subtraction, left to right

Example:

`2 + 3 * 4`

Multiply first:

`3 * 4 = 12`

Then add:

`2 + 12 = 14`

With parentheses:

`(2 + 3) * 4 = 5 * 4 = 20`

The parentheses change the answer.

## 5. Calculate a weighted sum

A weighted sum is central to neural networks.

Suppose:
- input x1 = 2
- input x2 = 3
- weight w1 = 4
- weight w2 = 5

Calculate:

`w1*x1 + w2*x2`

Substitute:

`4*2 + 5*3`

Multiply:

`8 + 15`

Add:

`23`

The weighted sum is 23.

## 6. Rounding and precision

A computer may store approximate decimal values. For example, some decimal fractions cannot be represented exactly in binary floating-point.

For learning, round only when appropriate. During calculations, keep extra digits until the final step.

## Common mistakes

- Doing addition before multiplication.
- Forgetting parentheses.
- Treating `-2^2` as the same as `(-2)^2`. Usually, `-2^2 = -(2^2) = -4`, while `(-2)^2 = 4`.
- Rounding too early.

## Practice

1. `8 + 3*2`
2. `(8 + 3)*2`
3. `-4 + 9`
4. `(-3)*(-6)`
5. `1/3 + 1/3`
6. If x1=2, x2=4, w1=3, w2=0.5, calculate `w1*x1 + w2*x2`.

## Answers

1. 14
2. 22
3. 5
4. 18
5. 2/3
6. `3*2 + 0.5*4 = 6 + 2 = 8`
