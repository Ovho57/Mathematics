# Lesson 19 — Overfitting, Regularization, and Generalization

## Underfitting

A model underfits when it is too simple or insufficiently trained to capture patterns.

Typical signs:
- training performance is poor,
- validation performance is also poor.

## Overfitting

A model overfits when it learns training examples too closely, including noise, and performs poorly on new data.

Typical signs:
- training loss is low,
- validation loss is much higher or starts increasing.

## Ways to reduce overfitting

### More suitable data
More representative training examples can improve generalization.

### Data augmentation
Create reasonable variations of training examples, such as small image rotations or crops. Augmentation must preserve the label.

### Early stopping
Stop training when validation performance stops improving.

### Regularization
Add a penalty for certain parameter values.

L2 regularization is often written:

`total_loss = data_loss + lambda * sum(weights^2)`

Lambda controls penalty strength. Biases are often treated differently from weights.

### Dropout
During training, randomly deactivate some activations. This discourages excessive reliance on individual neurons. Dropout is disabled during ordinary inference.

## Model capacity

A model with more parameters can represent more complex functions, but may require more data and careful training.

## Generalization is the goal

The goal is not simply memorizing training data. It is useful performance on examples the model has not seen.

## Practice

1. Training loss low, validation loss high: what may be happening?
2. What does early stopping use to decide when to stop?
3. What does lambda control in L2 regularization?
