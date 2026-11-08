# Lesson 11 — Training, Validation, and Testing

A model must be evaluated on examples it did not learn from.

## Three sets

- **Training:** used to adjust model parameters.
- **Validation:** used to compare models and tune choices.
- **Test:** used for final evaluation after decisions are complete.

A possible split is 70% training, 15% validation, 15% test, but the best split depends on the data.

## Why not evaluate only on training data?

A model may memorize its training examples. Strong training performance does not guarantee strong performance on new examples.

## Generalization

Generalization means performing well on new examples from the intended environment.

## Metrics

Classification:
- Accuracy = correct predictions / all predictions.
- Precision = among predicted positives, how many are true positives.
- Recall = among actual positives, how many were found.

Regression:
- MAE = average absolute error.
- MSE = average squared error.
- RMSE = square root of MSE.

Example: 18 correct out of 20:

`accuracy=18/20=0.9=90%`

Accuracy can mislead when classes are very imbalanced.

## Practice

1. Which set trains weights?
2. Why not repeatedly tune using the test set?
3. 45 correct out of 50: accuracy?
