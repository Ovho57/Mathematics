# Lesson 8 — Calculus: Derivatives and Gradients

Calculus helps us understand how changing one value affects another. Neural networks use derivatives to learn.

## 1. Change

Suppose:

`y=2*x`

If x changes from 3 to 4, y changes from 6 to 8.

The change in x is 1. The change in y is 2.

## 2. Slope

For a straight line:

`slope = change in y / change in x`

For `y=2*x+1`, the slope is 2.

## 3. Derivative

A derivative measures the instantaneous rate of change of a function.

We write:

`dy/dx`

Read this as “derivative of y with respect to x.”

For:

`y=x^2`

the derivative is:

`dy/dx = 2*x`

At x=3, the derivative is 6. This means the function's slope at that point is 6.

## 4. Common derivative rules

Constant:

`d/dx(c)=0`

Power rule:

`d/dx(x^n)=n*x^(n-1)`

Examples:
- derivative of x^2 is 2*x
- derivative of x^3 is 3*x^2
- derivative of 5*x is 5
- derivative of 7 is 0

Sum rule:

`d/dx(f(x)+g(x)) = f'(x)+g'(x)`

## 5. Chain rule

If one function is inside another, use the chain rule.

If:

`y = f(g(x))`

then:

`dy/dx = f'(g(x))*g'(x)`

Example:

`y=(3*x+1)^2`

Outer derivative: 2*(3*x+1)

Inner derivative: 3

Therefore:

`dy/dx = 2*(3*x+1)*3 = 6*(3*x+1)`

## 6. Partial derivatives

A function may depend on many variables:

`L(w,b)`

A partial derivative measures change with respect to one variable while holding the others fixed.

We write:
- `dL/dw` or `∂L/∂w`
- `dL/db` or `∂L/∂b`

## 7. Gradient

The gradient collects partial derivatives:

`gradient = [∂L/∂w1, ∂L/∂w2, ..., ∂L/∂wn]`

It points in the direction of steepest increase. To reduce loss, gradient descent moves in the opposite direction.

## 8. Gradient descent

Update a parameter:

`new_parameter = old_parameter - learning_rate * gradient`

Example:
- old weight = 5
- learning rate = 0.1
- gradient = 2

`new weight = 5 - 0.1*2 = 4.8`

If gradient is negative:

`new weight = 5 - 0.1*(-2) = 5.2`

## Practice

1. Derivative of x^4?
2. Derivative of 7*x+2?
3. If weight=3, learning rate=0.05, gradient=4, calculate the updated weight.

## Answers

1. 4*x^3
2. 7
3. 3 - 0.05*4 = 2.8
