# Lesson 9 — What Machine Learning Is

Machine learning (ML) is the study of algorithms that improve their performance by learning patterns from data.

## Traditional programming and ML

Traditional approach: programmer writes rules; program applies them.

Machine-learning approach: provide examples; a learning algorithm adjusts a model; the trained model predicts on new examples.

## Types of machine learning

**Supervised learning:** examples have target answers (labels). Example: image → cat or dog.

**Unsupervised learning:** no target label is provided; the algorithm finds structure, such as clusters.

**Reinforcement learning:** an agent acts, receives rewards, and learns a strategy.

## Regression and classification

Regression predicts a number (price, temperature, distance). Classification predicts a category (spam/not spam, cat/dog).

## Model, parameters, prediction

A model is a mathematical function:

`prediction = model(input; parameters)`

Parameters are values learned during training. Neural-network weights and biases are parameters.

## The learning loop

1. Initialize parameters.
2. Make predictions.
3. Calculate loss.
4. Calculate gradients.
5. Update parameters.
6. Repeat.

The model learns when parameter updates improve performance on relevant examples.

## Practice

1. Predicting temperature: regression or classification?
2. Cat/dog photo classification: regression or classification?
3. Which type uses labeled examples?
