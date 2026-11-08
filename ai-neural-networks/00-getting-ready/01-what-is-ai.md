# Lesson 0.2 — What Are AI, Machine Learning, and Deep Learning?

## Artificial intelligence

Artificial intelligence (AI) is the broad field of creating computer systems that perform tasks associated with intelligent behavior: recognizing patterns, understanding language, planning, or making predictions.

AI does not necessarily mean a machine thinks like a human. It means the system performs a task that we consider intelligent.

## Machine learning

Traditional programming often follows this pattern:

**Human writes rules + input → computer follows rules → output**

Machine learning uses a different approach:

**Examples + learning algorithm → model**

The model learns patterns from examples instead of requiring us to manually write every rule.

Imagine wanting a program to recognize handwritten digits. It is difficult to write a rule for every possible handwriting style. Instead, we provide many labeled examples and train a model to recognize patterns.

## Deep learning

Deep learning is a kind of machine learning that uses neural networks with multiple layers.

The word “deep” refers to the layers of computation—not to consciousness or human-like understanding.

## Important terms

- **Dataset:** a collection of examples.
- **Model:** the mathematical system that makes predictions.
- **Parameter:** a value the model learns, often called a weight or bias.
- **Training:** the process of adjusting parameters using examples.
- **Prediction:** the model's output for an input.
- **Inference:** using a trained model to make predictions.
- **Loss:** a number that measures how wrong a prediction is according to a chosen rule.
- **Algorithm:** a step-by-step procedure.

## The big picture

A simplified training cycle:

1. Give the model an input.
2. The model makes a prediction.
3. Compare prediction with the correct answer.
4. Calculate the loss.
5. Adjust parameters to reduce loss.
6. Repeat with many examples.

Later chapters explain every step mathematically.

## Checkpoint questions

1. How is machine learning different from manually writing every rule?
2. What does “deep” mean in deep learning?
3. What is the difference between training and inference?
