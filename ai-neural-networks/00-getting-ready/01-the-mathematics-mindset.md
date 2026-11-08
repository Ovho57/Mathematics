# Lesson 0.1 — The Mathematics Mindset

## 1. Mathematics describes relationships

Mathematics is a way to describe quantities, patterns, and relationships precisely.

Suppose you buy 3 notebooks, each costing 5 units of money. The total cost is:

\[
3 \times 5 = 15
\]

This is more than arithmetic. It describes a relationship:

\[
\text{total cost} = \text{number of notebooks} \times \text{price per notebook}
\]

We can generalize it:

\[
C = np
\]

Here, \(C\) is the total cost, \(n\) is the number of notebooks, and \(p\) is the price of one notebook.

The letters let us describe many situations with one formula.

## 2. Neural networks are functions

A function receives an input and produces an output according to a rule.

For example:

\[
f(x) = 2x + 3
\]

If the input is \(x=4\), then:

\[
f(4) = 2(4)+3 = 11
\]

Think of a function as a machine:

- Put in a value.
- Apply a rule.
- Receive an output.

A neural network is also a function, but its rule is built from many smaller mathematical operations. It contains adjustable numbers called **parameters**.

## 3. Parameters are adjustable values

Consider:

\[
f(x) = wx + b
\]

The input is \(x\). The numbers \(w\) and \(b\) are parameters:

- \(w\), the **weight**, controls how strongly the input affects the result.
- \(b\), the **bias**, shifts the result.

If \(x=2\), \(w=3\), and \(b=1\):

\[
f(2)=3(2)+1=7
\]

If we change the weight to 4:

\[
f(2)=4(2)+1=9
\]

The output changes because a parameter changed. Neural-network training is largely the process of finding useful parameter values.

## 4. Data can be represented as numbers

A computer needs numerical representations to perform calculations.

A single feature might be represented by a number:

\[
x=0.7
\]

Several features can be grouped into a vector:

\[
\mathbf{x} =
\begin{bmatrix}
0.7 \\
1.2 \\
-0.4
\end{bmatrix}
\]

This vector could represent three measured features of one example. The exact meaning depends on the dataset.

A collection of examples can be represented using a matrix. You will learn vectors and matrices in detail later.

## 5. Learning means reducing error

Imagine a network predicts a value, but its prediction is not correct.

- **Target:** the answer we want.
- **Prediction:** the answer the network produced.
- **Error:** the difference between them.
- **Loss:** a numerical measure of how bad the prediction is.

A simple error for one example is:

\[
e = \hat{y} - y
\]

where \(\hat{y}\) is the prediction and \(y\) is the target.

If the prediction is 8 and the target is 10:

\[
e = 8-10=-2
\]

The network can use a loss function to measure the error and calculus to determine how changing its parameters may reduce that loss.

## 6. The big picture

A simplified training process looks like this:

1. Receive input data.
2. Calculate a prediction.
3. Compare the prediction with the target.
4. Calculate the loss.
5. Determine how parameters affect the loss.
6. Adjust parameters.
7. Repeat with many examples.

The later chapters will explain every mathematical step in this process.

## Practice

1. Evaluate \(f(x)=3x+2\) when \(x=5\).
2. In \(f(x)=wx+b\), identify the input and parameters.
3. If \(\hat{y}=12\) and \(y=9\), calculate \(e=\hat{y}-y\).
4. Explain why changing a weight can change a neural network’s prediction.
5. Why does a network need a way to measure its prediction error?

## Answers

1. \(3(5)+2=17\).
2. Input: \(x\). Parameters: \(w\) and \(b\).
3. \(12-9=3\).
4. The weight changes how strongly an input contributes to the calculation.
5. The error measure provides a way to evaluate predictions and guide learning.

### Key idea

A neural network is a function whose parameters are adjusted using data. Mathematics explains the function, the error, and how to improve its parameters.
