# Mathematics for AI and Neural Networks
## From Zero to Building Neural Networks from Scratch

This book teaches the mathematics behind artificial intelligence, machine learning, and neural networks—not just formulas to memorize. The goal is to understand what each mathematical operation means, why neural networks use it, and how to implement it yourself in Python.

**You do not need to know all the mathematics before starting.** Learn the foundations in order, then revisit them as the neural-network chapters use them.

## What you will be able to do

By the end, you should be able to:

- Explain the mathematical ideas behind machine learning and neural networks.
- Represent data, weights, biases, and layers using vectors and matrices.
- Calculate a neuron’s output by hand and in Python.
- Understand activation functions, loss functions, gradients, and optimization.
- Explain backpropagation instead of treating it as magic.
- Build a small neural network from scratch using Python and NumPy.
- Train, evaluate, debug, and improve a neural network.
- Understand the mathematical foundations of deeper networks and introductory modern AI.

## How to study

1. Read one lesson slowly.
2. Work through each example with paper and pencil.
3. Try the exercises before looking at answers.
4. Write small Python experiments to verify your calculations.
5. Explain the concept in your own words.
6. Do not move on just because a formula looks familiar—make sure you can use it.

## Book map

### Part 0 — Getting ready
- [0.0 How to use this book](./00-getting-ready/00-how-to-use-this-book.md)
- [0.1 The mathematics mindset](./00-getting-ready/01-the-mathematics-mindset.md)

### Part 1 — Number and algebra foundations
- Numbers, arithmetic, fractions, decimals, and percentages
- Variables and expressions
- Equations and inequalities
- Exponents, roots, and logarithms
- Functions, graphs, domain, and range
- Summation notation (Σ)
- Rearranging formulas

### Part 2 — Coordinate geometry and graphs
- The Cartesian plane
- Coordinates and points
- Slope and straight lines
- Graphs of functions
- Distance and geometric intuition
- Reading plots and visualizing data

### Part 3 — Trigonometry
- Angles and radians
- Sine, cosine, and tangent
- Unit circle intuition
- Trigonometric functions
- Why periodic functions matter

### Part 4 — Vectors
- What a vector is
- Vector notation and components
- Vector addition and subtraction
- Scalar multiplication
- Magnitude and direction
- Dot product and its geometric meaning
- Linear combinations
- Vector spaces (intuition first)

### Part 5 — Matrices and linear algebra
- What matrices represent
- Matrix dimensions and indexing
- Matrix addition and scalar multiplication
- Matrix-vector multiplication
- Matrix-matrix multiplication
- Transpose
- Identity matrix
- Linear transformations
- Systems of linear equations
- Rank, span, and independence (introductory)
- Eigenvalues and eigenvectors (later, optional foundation)

### Part 6 — Probability
- What probability means
- Events and sample spaces
- Conditional probability
- Independence
- Bayes’ theorem
- Random variables
- Expected value and variance
- Common probability distributions
- Why AI predictions are not always certain

### Part 7 — Statistics and data
- Population and sample
- Mean, median, and mode
- Variance and standard deviation
- Covariance and correlation
- Data normalization and standardization
- Sampling and bias
- Training, validation, and test sets

### Part 8 — Calculus
- What a function is (review)
- Limits and continuity
- Average rate of change
- Derivatives and slope
- Derivative rules
- Chain rule
- Partial derivatives
- Gradients
- Multivariable functions
- Directional intuition
- Integrals and area (useful background)
- Why gradients tell us how to update neural-network parameters

### Part 9 — Optimization
- What optimization means
- Loss and objective functions
- Parameters and hyperparameters
- Gradient descent
- Learning rate
- Stochastic and mini-batch gradient descent
- Momentum and adaptive optimizers (conceptual)
- Local minima, saddle points, and flat regions

### Part 10 — Neural-network mathematics
- From a biological metaphor to a mathematical model
- The artificial neuron
- Weighted sums and bias
- Activation functions: sigmoid, tanh, ReLU, softmax
- Layers and network notation
- Forward propagation
- Loss functions: MSE and cross-entropy
- Derivatives through a network
- Backpropagation from first principles
- Gradient checking
- Training loop
- Overfitting, underfitting, and regularization
- Initialization and vanishing/exploding gradients

### Part 11 — Build neural networks from scratch
- Python and NumPy refresher
- A single neuron
- A network with one hidden layer
- Forward pass
- Loss calculation
- Backpropagation implementation
- Gradient descent update
- Training on a tiny dataset
- Classification and regression
- Evaluation and debugging
- Build a reusable neural-network class

### Part 12 — Beyond the basics
- Multi-class classification and softmax
- Embeddings and vector representations
- Convolutional networks (math intuition)
- Recurrent networks (math intuition)
- Attention and the Transformer (introductory)
- Numerical stability
- What the mathematics does not explain by itself

### Projects
1. Predict a number using linear regression.
2. Implement a single artificial neuron.
3. Train a neural network on XOR.
4. Build a handwritten-digit classifier (with a small dataset).
5. Compare activation functions and learning rates.
6. Explain and visualize a training run.

## Suggested prerequisites

Start with basic arithmetic and algebra. If a topic is unfamiliar, study its chapter before the neural-network chapter that uses it. Calculus and linear algebra are taught inside this book.

## Important note

This is a learning path, not a promise that every advanced AI topic can be mastered immediately. Build understanding step by step. Neural networks are learnable when their mathematics is broken into small pieces.
