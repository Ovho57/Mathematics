# Mathematics for AI and Neural Networks — The Complete Beginner-to-Builder Textbook

**A practical textbook:** learn the mathematics, understand what it means, calculate examples by hand, then implement it in Python.

> **Equation display rule:** This book uses plain-text equations inside backticks. They are intentionally written this way so the operations remain readable on GitHub, phones, Markdown previews, and text-only viewers. Read `*` as multiply, `/` as divide, `**` as “raised to the power,” and `sqrt(x)` as square root of x.

---

# How to use this textbook

Follow the chapters in order. For each chapter:
1. Read the explanation.
2. Copy the worked example and calculate each line yourself.
3. Complete the exercises without looking at the answers.
4. Explain the idea aloud or in your own words.
5. Use Python only after you understand the hand calculation.

You do not need to be “naturally good at maths.” You need practice and a willingness to check each step.

# PART I — THE MATHEMATICS FOUNDATIONS

## Chapter 1 — Numbers and arithmetic

A neural network is a program that performs many numerical operations. The basic operations are addition, subtraction, multiplication, division, powers, and comparisons.

### Number types
- Natural numbers: 1, 2, 3, …
- Whole numbers: 0, 1, 2, 3, …
- Integers: …, -2, -1, 0, 1, 2, …
- Rational numbers: numbers expressible as a fraction, such as 3/4 or -5/2.
- Real numbers: rational numbers plus values such as sqrt(2) and pi.

Neural-network weights can be positive, negative, or zero. A negative weight can make an input contribute in the opposite direction.

### Arithmetic with negative numbers
- 5 + (-2) = 3
- -5 + (-2) = -7
- (-3) * 4 = -12
- (-3) * (-4) = 12
- 7 - (-3) = 7 + 3 = 10

### Fractions and decimals
- 1/2 = 0.5
- 1/4 = 0.25
- 3/4 = 0.75
- 0.2 * 0.3 = 0.06

To add fractions, use a common denominator:
1/2 + 1/3 = 3/6 + 2/6 = 5/6.

### Order of operations
Use parentheses first, powers next, multiplication/division from left to right, then addition/subtraction from left to right.

3 + 2 * 5 = 3 + 10 = 13  
(3 + 2) * 5 = 5 * 5 = 25

### Worked AI example
A weighted calculation:
z = 2 * 0.5 + (-3) * 0.2 + 1  
z = 1 - 0.6 + 1  
z = 1.4

This calculation is the core of a simple artificial neuron.

### Practice
1. 17 - 25
2. (-6) * (-4)
3. 7 + 3 * 4
4. 1/4 + 1/2
5. 15% of 200
6. 3 * 0.4 + 2 * 0.1 - 1

Answers: -8, 24, 19, 3/4, 30, 0.4.

## Chapter 2 — Variables, expressions, and equations

A **variable** is a symbol that stands for a value. For example, x may represent an unknown number.

An **expression** combines numbers, variables, and operations:
- 3x + 2 means 3 multiplied by x, then add 2.
- x**2 means x multiplied by itself.
- 2a + 4b is a linear expression in a and b.

An **equation** says two expressions are equal:
3x + 2 = 11.

Solve by keeping both sides balanced:
3x + 2 = 11  
3x = 11 - 2 = 9  
x = 9 / 3 = 3.

### Substitution
If x = 4, then 2x + 5 = 2 * 4 + 5 = 13.

### AI connection
Neural-network formulas use variables:
- x = input
- w = weight
- b = bias
- z = weighted sum

A neuron is often written:
z = w*x + b.

The symbols are not mysterious; they are placeholders for values.

### Practice
1. Solve 2x + 3 = 13.
2. If a = 2 and b = 5, calculate 3a + b.
3. Solve 5x = 35.
4. If w = -2, x = 4, b = 3, calculate w*x + b.

Answers: x=5; 11; x=7; -5.

## Chapter 3 — Powers, roots, and logarithms

A power is repeated multiplication:
2**3 = 2 * 2 * 2 = 8.

Rules:
- x**a * x**b = x**(a+b)
- x**a / x**b = x**(a-b), for x != 0
- (x**a)**b = x**(a*b)
- x**0 = 1, for x != 0
- x**(-a) = 1/(x**a)

A root reverses a power:
sqrt(25) = 5 because 5**2 = 25.

A logarithm answers: “What exponent gives this number?”
log base 2 of 8 = 3 because 2**3 = 8.

Natural logarithm ln(x) is log base e. It appears in probability and cross-entropy loss.

### AI connection
- Squared error uses powers.
- Sigmoid and softmax use exponentials.
- Cross-entropy uses logarithms.

Practice:
1. 2**5
2. 10**(-3)
3. sqrt(144)
4. log base 3 of 27

Answers: 32; 0.001; 12; 3.

## Chapter 4 — Functions and graphs

A **function** takes an input and produces an output. Write y = f(x).

Example:
f(x) = 2x + 1.

If x=3:
f(3) = 2*3 + 1 = 7.

The input is x; the output is f(x). A graph shows how output changes as input changes.

### Domain and range
- Domain: allowed inputs.
- Range: outputs the function can produce.

### AI connection
An activation function transforms a neuron's weighted sum:
output = activation(z).

The network is a composition of functions: one function's output becomes the next function's input.

## Chapter 5 — Coordinate geometry and slope

A coordinate is written (x, y). The x-coordinate moves horizontally; y moves vertically.

Slope measures vertical change divided by horizontal change:
slope = (y2 - y1) / (x2 - x1).

For points (1, 2) and (3, 6):
slope = (6 - 2)/(3 - 1) = 4/2 = 2.

A line can be written:
y = m*x + c,
where m is slope and c is the y-intercept.

### AI connection
A model may learn a slope and intercept:
prediction = w*x + b.
This is linear regression and also the basic form of a single neuron before activation.

## Chapter 6 — Summation notation

The Greek capital sigma, Σ, means “add a sequence of terms.”

Example:
Σ from i=1 to 3 of x_i means x_1 + x_2 + x_3.

If values are 2, 4, 6:
sum = 2 + 4 + 6 = 12.

A neuron with several inputs:
z = Σ(w_i*x_i) + b.

In plain English: multiply each input by its matching weight, add all those products, then add the bias.

This notation is essential because neural networks may have hundreds or thousands of inputs.

# PART II — VECTORS AND MATRICES

## Chapter 7 — Vectors

A vector is an ordered list of numbers. It can represent features of one example.

Example:
x = [2, 5, 1].

Vector addition is component-by-component:
[1, 2] + [3, 4] = [4, 6].

Scalar multiplication:
3 * [2, 4] = [6, 12].

### Magnitude
For vector [3, 4]:
magnitude = sqrt(3**2 + 4**2) = sqrt(9+16) = 5.

### Dot product
Multiply matching entries and add:
[2, 3] dot [4, 5] = 2*4 + 3*5 = 8+15 = 23.

The dot product is the compact form of a neuron's weighted sum:
z = w dot x + b.

## Chapter 8 — Matrices

A matrix is a rectangular grid of numbers.

A 2-by-3 matrix has 2 rows and 3 columns:
A = [[1, 2, 3],
     [4, 5, 6]].

Dimensions matter. A matrix with 2 rows and 3 columns is called 2 x 3.

### Matrix-vector multiplication
Let:
A = [[1, 2],
     [3, 4]]
x = [5, 6].

Multiply each row by the vector:
first result = 1*5 + 2*6 = 17  
second result = 3*5 + 4*6 = 39.

Therefore:
A*x = [17, 39].

### Why matrices are used in neural networks
A layer with many neurons performs many weighted sums. Instead of calculating each neuron separately, we group weights into a matrix.

For a dense layer:
z = W*x + b.

- W = matrix of weights
- x = input vector
- b = bias vector
- z = vector of weighted sums

### Matrix multiplication rule
For A of shape (m,n) and B of shape (n,p), the product AB has shape (m,p). The inner dimensions must match.

## Chapter 9 — Linear transformations

A matrix can transform vectors: rotate, scale, reflect, or combine dimensions.

A neural layer's matrix multiplication transforms an input representation into a new representation.

Important distinction: matrix multiplication alone is linear. Adding bias makes it affine. Applying a nonlinear activation allows networks to model complicated relationships.

If every layer were only linear, stacking layers would still equal one linear transformation. Nonlinear activations are what give ordinary neural networks much of their expressive power.

# PART III — PROBABILITY AND STATISTICS

## Chapter 10 — Probability

Probability describes uncertainty. Values range from 0 to 1:
- 0 = impossible under the model
- 1 = certain under the model
- 0.5 = half probability

For equally likely outcomes:
probability = favorable outcomes / total outcomes.

A fair six-sided die:
P(rolling 4) = 1/6.

### Conditional probability
P(A | B) means probability of A when B is known:
P(A | B) = P(A and B) / P(B), when P(B)>0.

### Bayes' theorem
P(A | B) = P(B | A)*P(A) / P(B).

It updates a probability using evidence.

### AI connection
Classification models often output scores interpreted as probabilities, but those probabilities can be poorly calibrated. A model's confidence is not automatically truth.

## Chapter 11 — Random variables and expected value

A random variable assigns a number to an uncertain outcome.

Expected value is the long-run average:
E[X] = Σ x_i * P(X=x_i).

Example: a fair die:
E[X] = (1+2+3+4+5+6)/6 = 3.5.

Variance measures spread:
Var(X) = E[(X - mean)**2].

Standard deviation:
SD = sqrt(variance).

These concepts help describe data and prediction uncertainty.

## Chapter 12 — Statistics and datasets

Mean:
mean = sum of values / number of values.

Example values 2, 4, 6:
mean = (2+4+6)/3 = 4.

Median is the middle sorted value. Mode is the most frequent value.

### Data splitting
- Training set: used to fit parameters.
- Validation set: used to choose settings and compare models.
- Test set: used for a final, unbiased evaluation.

Do not repeatedly tune using the test set. That leaks information and makes reported performance misleading.

### Scaling features
Min-max scaling:
scaled = (x - minimum)/(maximum - minimum).

Standardization:
z = (x - mean)/standard deviation.

Scaling can make optimization easier when features have very different ranges.

# PART IV — CALCULUS AND LEARNING

## Chapter 13 — Rates of change and derivatives

A derivative measures how quickly a function changes as its input changes. It is the slope at a point.

For f(x) = x**2:
- f(2) = 4
- f(3) = 9
- average change from 2 to 3 = (9-4)/(3-2) = 5.

The derivative at x=2 is 4. It describes the instantaneous slope there.

Notation:
- f'(x)
- dy/dx

### Common derivative rules
- derivative of constant c = 0
- derivative of x = 1
- derivative of x**n = n*x**(n-1)
- derivative of c*f(x) = c*f'(x)
- derivative of f(x)+g(x) = f'(x)+g'(x)

Examples:
d/dx(x**2) = 2x  
d/dx(3x**2 + 2x + 1) = 6x + 2.

## Chapter 14 — Chain rule

The chain rule differentiates a function inside another function.

If y = f(g(x)):
dy/dx = f'(g(x)) * g'(x).

Example:
y = (3x + 2)**2.

Outer function: square. Inner function: 3x+2.
Derivative:
2*(3x+2)*3 = 6*(3x+2) = 18x+12.

### Why this matters for neural networks
A network is a chain of functions:
input -> layer 1 -> layer 2 -> output.

To determine how an early weight affects the final loss, we apply the chain rule through the later calculations. This is the core idea behind backpropagation.

## Chapter 15 — Partial derivatives and gradients

A function may depend on many variables:
L(w,b).

A partial derivative asks how L changes when one variable changes while the others are held fixed.

Gradient:
∇L = [partial L/partial w, partial L/partial b, ...].

The gradient points toward the direction of steepest increase locally. To reduce loss, move in the opposite direction.

## Chapter 16 — Gradient descent

Goal: find parameter values that make loss small.

Update rule:
new_parameter = old_parameter - learning_rate * gradient.

For weight w:
w_new = w_old - η*(dL/dw).

η (eta) is the learning rate.

Example:
w = 2, gradient = 0.5, learning rate = 0.1:
w_new = 2 - 0.1*0.5 = 1.95.

If the learning rate is too large, updates may overshoot. If too small, training may be slow.

# PART V — NEURAL NETWORKS

## Chapter 17 — What is a neural network?

A neural network is a mathematical function made by composing layers of simple operations. It learns by adjusting weights and biases to reduce a loss function on examples.

A network is not literally a human brain. “Neuron” and “layer” are mathematical/computational metaphors.

A basic feed-forward network:
input -> hidden layer(s) -> output.

- Input layer receives features.
- Hidden layers learn intermediate representations.
- Output layer produces the final prediction.

## Chapter 18 — The artificial neuron

A neuron receives inputs x_1, x_2, ..., x_n. Each input has a weight w_i.

First calculate:
z = w_1*x_1 + w_2*x_2 + ... + w_n*x_n + b.

Then apply activation:
a = φ(z).

Here:
- x = input
- w = learned weight
- b = learned bias
- z = weighted sum before activation
- φ = activation function
- a = neuron output

### Worked example
Inputs: x1=2, x2=3.  
Weights: w1=0.5, w2=-1.  
Bias: b=2.

z = 0.5*2 + (-1)*3 + 2  
z = 1 - 3 + 2  
z = 0.

If activation is ReLU:
ReLU(0) = max(0,0) = 0.

## Chapter 19 — Activation functions

Activation functions add nonlinearity.

### ReLU
ReLU(z) = max(0,z).
- If z is positive, output z.
- If z is negative, output 0.

Examples: ReLU(3)=3; ReLU(-2)=0.

### Sigmoid
sigmoid(z) = 1/(1 + exp(-z)).
Its output is between 0 and 1. It is often used for a binary-classification output.

### Tanh
tanh(z) = (exp(z)-exp(-z))/(exp(z)+exp(-z)).
Its output lies between -1 and 1.

### Softmax
For scores z_i:
softmax(z_i) = exp(z_i) / sum_j exp(z_j).

Softmax converts a vector of scores into values that sum to 1. It is commonly used for multi-class classification.

## Chapter 20 — Layers and network shapes

A dense (fully connected) layer connects every input unit to every output unit.

Suppose:
- input has 3 features
- hidden layer has 4 neurons
- output layer has 2 neurons

Shapes:
- input x: (3,)
- first layer weight matrix W1: (4,3)
- first bias b1: (4,)
- hidden result z1 and a1: (4,)
- second weight matrix W2: (2,4)
- second bias b2: (2,)
- output z2: (2,)

The rule is:
W shape = (number of neurons in this layer, number of inputs to each neuron).

This helps you catch dimension mistakes.

### Layer calculation
z1 = W1*x + b1  
a1 = activation(z1)  
z2 = W2*a1 + b2  
output = output_activation(z2).

Each row of W represents one neuron's weights.

## Chapter 21 — Forward propagation

Forward propagation means passing input data through the network to compute a prediction.

For a network with one hidden layer:
1. Receive input x.
2. Calculate z1 = W1*x + b1.
3. Calculate a1 = ReLU(z1).
4. Calculate z2 = W2*a1 + b2.
5. Calculate prediction = output activation(z2).

Forward propagation uses the current parameters. It does not itself update them.

## Chapter 22 — Loss functions

A loss function measures how wrong a prediction is. Training attempts to reduce loss.

### Mean squared error (MSE)
For prediction y_hat and target y:
MSE = (1/N) * sum over examples of (y_hat - y)**2.

Example:
prediction = 4, target = 6:
squared error = (4-6)**2 = 4.

MSE is often used for regression.

### Binary cross-entropy
For target y in {0,1} and predicted probability p:
loss = -[y*ln(p) + (1-y)*ln(1-p)].

If y=1, loss = -ln(p): high p is rewarded, low p is penalized.
If y=0, loss = -ln(1-p): low p is rewarded.

### Categorical cross-entropy
For one-hot target values and predicted class probabilities:
loss = -sum_i y_i*ln(p_i).

It penalizes assigning low probability to the correct class.

## Chapter 23 — Backpropagation: the idea

Backpropagation calculates how much each parameter contributes to the loss.

It does not mean “the network thinks backward.” It is an efficient application of the chain rule.

Process:
1. Run forward propagation.
2. Calculate loss.
3. Calculate derivatives of loss with respect to output values.
4. Use chain rule to move gradients backward through layers.
5. Calculate gradient for every weight and bias.
6. Update parameters using gradient descent.

For a simple weight:
w_new = w_old - learning_rate*(dLoss/dw).

The gradient tells us how the loss changes if a parameter changes slightly.

## Chapter 24 — Backpropagation through a simple neuron

Let:
z = w*x + b  
a = sigmoid(z)  
L = loss(a,y).

By chain rule:
dL/dw = (dL/da)*(da/dz)*(dz/dw).

Since z = w*x+b:
dz/dw = x.

Thus:
dL/dw = (dL/da)*(da/dz)*x.

And:
dL/db = (dL/da)*(da/dz),
because dz/db = 1.

For sigmoid:
sigmoid'(z) = sigmoid(z)*(1-sigmoid(z)).

This is a simplified example of how gradients flow through a network.

## Chapter 25 — Training loop

A standard training loop:
1. Initialize weights and biases.
2. Select a batch of training examples.
3. Forward pass: compute predictions.
4. Compute loss.
5. Backward pass: compute gradients.
6. Update weights and biases.
7. Repeat for many batches and epochs.
8. Evaluate on validation data.

An epoch means one full pass through the training dataset. A batch is a subset used for one update.

## Chapter 26 — Why networks need multiple layers

A single linear neuron can only represent limited relationships. Hidden layers and nonlinear activations allow a network to combine simple features into more complex patterns.

Example intuition:
- Early layer: detect simple combinations.
- Middle layer: combine those into more useful patterns.
- Later layer: use those representations to predict.

This is a conceptual analogy, not a guarantee that each neuron learns a human-readable feature.

## Chapter 27 — Overfitting, underfitting, and regularization

- Underfitting: model is too simple or not trained enough.
- Overfitting: model memorizes training patterns and performs poorly on unseen examples.
- Generalization: performance on new examples.

Ways to reduce overfitting:
- More representative data
- Train/validation separation
- Weight decay (L2 regularization)
- Dropout in suitable networks
- Early stopping
- Smaller model when appropriate

L2 regularization adds a penalty related to squared weights:
total_loss = data_loss + λ*sum(weights**2).

## Chapter 28 — Initialization and gradient problems

Weights should not all start at the same value. Identical initial weights can make neurons learn identical behavior.

Common strategies include Xavier/Glorot and He initialization, chosen based on activation and architecture.

### Vanishing gradients
Gradients become very small as they pass through many layers. Early layers may learn slowly.

### Exploding gradients
Gradients become extremely large, causing unstable updates.

Possible approaches:
- suitable initialization
- ReLU-family activations in many hidden layers
- normalization methods
- residual connections in deep architectures
- gradient clipping where appropriate

# PART VI — BUILD IT WITH PYTHON

## Chapter 29 — Python and NumPy essentials

You should know:
- variables
- lists
- functions
- loops
- indexing
- basic classes (optional at first)
- NumPy arrays and shapes

Example:
```python
import numpy as np

x = np.array([2.0, 3.0])
w = np.array([0.5, -1.0])
b = 2.0

z = np.dot(w, x) + b
print(z)  # 0.0
```

Always inspect array shapes:
```python
print(x.shape)
print(w.shape)
```

## Chapter 30 — Build one neuron

```python
import numpy as np

def relu(x):
    return np.maximum(0, x)

def neuron(inputs, weights, bias):
    z = np.dot(weights, inputs) + bias
    return relu(z)

x = np.array([2.0, 3.0])
w = np.array([0.5, -1.0])
b = 2.0

print(neuron(x, w, b))
```

The code mirrors the math:
- np.dot(weights, inputs) calculates the weighted sum.
- + bias adds the bias.
- relu applies the activation.

## Chapter 31 — Build a dense layer

```python
import numpy as np

def dense(inputs, weights, biases):
    # weights shape: (number_of_neurons, number_of_inputs)
    # inputs shape: (number_of_inputs,)
    # biases shape: (number_of_neurons,)
    return weights @ inputs + biases

def relu(x):
    return np.maximum(0, x)

x = np.array([1.0, 2.0, 3.0])
W = np.array([
    [0.2, 0.4, -0.1],
    [-0.3, 0.5, 0.2]
])
b = np.array([0.1, -0.2])

z = dense(x, W, b)
a = relu(z)
print("z:", z)
print("a:", a)
```

Here W has shape (2,3): two neurons, each receiving three input values.

## Chapter 32 — A complete network's forward pass

```python
import numpy as np

def relu(x):
    return np.maximum(0, x)

def forward(x, W1, b1, W2, b2):
    hidden = relu(W1 @ x + b1)
    output = W2 @ hidden + b2
    return output

# 2 inputs -> 3 hidden neurons -> 1 output
x = np.array([0.4, 0.8])
W1 = np.array([
    [0.2, -0.1],
    [0.7, 0.3],
    [-0.4, 0.5]
])
b1 = np.array([0.0, 0.1, 0.2])
W2 = np.array([[0.5, -0.2, 0.4]])
b2 = np.array([0.1])

print(forward(x, W1, b1, W2, b2))
```

This is a forward pass only. The network has not learned yet because no training updates have occurred.

## Chapter 33 — Numerical gradient checking

Before trusting a manually implemented gradient, compare it with a numerical estimate.

For small epsilon:
numerical_gradient ≈ (L(w+epsilon)-L(w-epsilon))/(2*epsilon).

This is called a central finite-difference estimate. It is useful for debugging. Do not use it as the main training method for large networks because it is expensive.

## Chapter 34 — A complete learning project

Build a tiny binary classifier:
1. Create a small labeled dataset.
2. Split into train and validation.
3. Choose input size, hidden size, and output size.
4. Initialize weights.
5. Implement forward pass.
6. Implement loss.
7. Implement backpropagation.
8. Implement gradient descent.
9. Track loss over epochs.
10. Evaluate on validation examples.
11. Inspect incorrect predictions.
12. Change one setting at a time and compare.

Start with a tiny dataset so every calculation can be inspected. Then use larger datasets.

# PART VII — MORE MODERN NEURAL NETWORKS

## Chapter 35 — Multi-class classification and softmax

A multi-class model outputs one score per class. Softmax converts scores into a distribution.

Example scores:
[2.0, 1.0, 0.1].

Softmax:
p_i = exp(score_i) / sum_j exp(score_j).

The probabilities sum to 1. The highest probability is the model's chosen class, but it can still be wrong.

For numerical stability, subtract the largest score before exponentiating:
softmax(z) = softmax(z - max(z)).
This does not change the result and helps prevent overflow.

## Chapter 36 — Embeddings

An embedding maps an item—such as a word or token—to a vector.

Instead of representing a word as a huge one-hot vector, a model learns a compact list of numbers:
token -> [v1, v2, ..., vd].

Embeddings allow similarity and relationships to be represented geometrically. The dimensions are learned and usually do not have simple human labels.

## Chapter 37 — Convolutional neural networks (CNNs)

CNNs are often used for image data. A small filter (kernel) moves across an image and computes local weighted combinations.

Simplified 1D example:
input = [1, 2, 3, 4]  
kernel = [1, 0]  
valid outputs = [1*1+2*0, 2*1+3*0, 3*1+4*0] = [1,2,3].

CNNs use shared filters, which reduces parameters and captures local patterns.

## Chapter 38 — Recurrent neural networks (RNNs)

RNNs process sequences. A hidden state carries information from one step to the next.

Simplified form:
h_t = activation(W_x*x_t + W_h*h_(t-1) + b).

- x_t = input at time t
- h_(t-1) = previous hidden state
- h_t = updated hidden state

RNNs are important historically and conceptually. Modern sequence models often use other architectures.

## Chapter 39 — Attention and Transformers: introductory mathematics

Attention lets each token combine information from other tokens.

A Transformer creates:
- Query (Q)
- Key (K)
- Value (V)

Scaled dot-product attention:
Attention(Q,K,V) = softmax(Q*K^T / sqrt(d_k))*V.

Intuition:
1. Compare queries with keys using dot products.
2. Scale the scores.
3. Softmax scores into weights.
4. Use those weights to combine value vectors.

This formula is a starting point; understanding Transformers fully also requires tokenization, embeddings, positional information, multiple heads, feed-forward layers, residual connections, and normalization.

## Chapter 40 — Numerical stability and limits of the math

Computers store approximate floating-point numbers. Not every decimal is represented exactly.

Important habits:
- avoid subtracting nearly equal values when possible
- use stable softmax and log-sum-exp implementations
- check for NaN and infinity
- use appropriate data types
- monitor loss and gradients
- remember that a mathematically valid formula can still be numerically unstable

Mathematics explains the model's calculations, but it does not by itself guarantee good data, fairness, interpretability, or reliable predictions.

# FINAL REVIEW — THE COMPLETE NEURAL NETWORK IN ONE VIEW

For input vector x:

1. First hidden layer:
z1 = W1*x + b1  
a1 = activation(z1)

2. Next layer:
z2 = W2*a1 + b2  
a2 = activation(z2)

3. Output:
prediction = output_layer(a_last)

4. Loss:
L = loss(prediction, target)

5. Backpropagation:
calculate gradients dL/dW and dL/db using the chain rule.

6. Update:
W_new = W_old - learning_rate*dL/dW  
b_new = b_old - learning_rate*dL/db

7. Repeat over training batches and epochs.

That is the core training cycle: **forward pass → loss → backward pass → update → repeat**.

# Glossary

- **Activation:** nonlinear transformation of a neuron's weighted sum.
- **Batch:** a group of examples used for one update.
- **Bias:** trainable additive value in a neuron.
- **Derivative:** local rate of change.
- **Epoch:** one pass through the training dataset.
- **Feature:** input measurement or attribute.
- **Forward propagation:** calculate a prediction through the network.
- **Gradient:** collection of derivatives with respect to parameters.
- **Hidden layer:** layer between input and output.
- **Learning rate:** size of parameter updates.
- **Loss:** numerical measure of prediction error.
- **Neuron:** weighted-sum calculation followed by an activation.
- **Parameter:** value learned from data, usually weight or bias.
- **Backpropagation:** chain-rule method for calculating gradients.
- **Weight:** learned multiplier controlling an input's contribution.

# Next steps

This textbook introduces the full path. The next improvement should be to expand each chapter into its own detailed lesson with more worked examples, diagrams, exercises, and answer explanations. Do not treat the compact overview chapters as a substitute for practice.
