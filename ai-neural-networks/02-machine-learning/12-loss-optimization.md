# Lesson 12 — Loss Functions and Optimization

Loss converts prediction errors into a number that training tries to reduce.

## Prediction error

`error = prediction - target`

Prediction=8, target=10:

`error=8-10=-2`

## Mean absolute error

`MAE = average(abs(prediction - target))`

Errors -2, 1, 3 become absolute errors 2, 1, 3:

`MAE=(2+1+3)/3=2`

## Mean squared error

`MSE = average((prediction-target)^2)`

For errors -2, 1, 3:

`MSE=(4+1+9)/3=14/3`

Squaring makes larger errors count more strongly.

## Binary cross-entropy

For binary target y and predicted probability p:

`loss = -[y*log(p) + (1-y)*log(1-p)]`

If y=1:

`loss=-log(p)`

Assigning high probability to the correct class produces low loss; assigning very low probability produces high loss.

## Optimization and gradient descent

`parameter = parameter - learning_rate * gradient`

Learning rate controls step size. Too small may make training slow; too large may cause overshooting or instability.

## Batch types

- Batch gradient descent: all examples per update.
- Stochastic gradient descent: one example per update.
- Mini-batch: small group per update (widely used).

## Practice

1. Prediction=12, target=9: error and squared error?
2. Why use a loss function?
3. What might a huge learning rate cause?
