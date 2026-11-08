# Lesson 1 — Numbers and Arithmetic: The Ground Floor of AI Mathematics

> **Goal:** Understand the number operations that appear inside every neural network calculation. No previous AI mathematics is required.

## 1. Why start here?

A neural network is built from calculations. It adds numbers, multiplies numbers, compares values, and repeatedly applies formulas.

A neural network may eventually contain millions or billions of parameters, but the basic operations are still arithmetic.

For example, a simple artificial neuron might calculate:

\[
z = 2.5(0.4) + 0.8
\]

This means:
1. Multiply 2.5 by 0.4.
2. Add 0.8.
3. Use the result as the neuron's input to its activation function.

If multiplication and addition are confusing, neural-network equations will be difficult. So we will make those operations clear first.

---

## 2. The main kinds of numbers

### Natural numbers

Counting numbers:

\[
1, 2, 3, 4, 5, \ldots
\]

Depending on convention, some definitions include zero.

### Whole numbers

Non-negative integers:

\[
0, 1, 2, 3, 4, \ldots
\]

### Integers

Positive numbers, negative numbers, and zero:

\[
\ldots, -3, -2, -1, 0, 1, 2, 3, \ldots
\]

Negative numbers matter in AI. A weight can be negative, and a negative weight means the input can influence the neuron in the opposite direction.

### Fractions

A fraction represents part of a whole:

\[
\frac{3}{4}
\]

The top number is the **numerator**. The bottom number is the **denominator**. Here, 3 out of 4 equal parts are represented.

### Decimals

Fractions can be written as decimals:

\[
\frac{1}{2}=0.5, \qquad \frac{1}{4}=0.25
\]

AI calculations commonly use decimal numbers.

### Real numbers

Real numbers include integers, fractions, decimals, and irrational values such as \(\sqrt{2}\). Most numbers used in basic neural-network mathematics are treated as real numbers.

---

## 3. Addition and subtraction

Addition combines quantities:

\[
4+3=7
\]

Subtraction measures a difference:

\[
7-4=3
\]

Subtraction can also produce a negative result:

\[
4-7=-3
\]

### Why subtraction matters in AI

Suppose a model predicts 6, but the correct target is 10. The difference is:

\[
6-10=-4
\]

This tells us the prediction is 4 below the target. Later, we will study loss functions that measure prediction errors more carefully.

### Adding negative numbers

Think of a number line.

- Adding a positive number moves right.
- Adding a negative number moves left.

Examples:

\[
5+(-2)=3
\]

\[
-3+(-4)=-7
\]

\[
-5+8=3
\]

**Rule:** Subtracting a number is the same as adding its opposite.

\[
7-(-3)=7+3=10
\]

---

## 4. Multiplication

Multiplication is repeated addition when dealing with whole numbers:

\[
3\times4=4+4+4=12
\]

Multiplication also scales a number. For example:

\[
2\times 5=10
\]

### Signs when multiplying

| Calculation | Result |
|---|---:|
| Positive × Positive | Positive |
| Negative × Positive | Negative |
| Positive × Negative | Negative |
| Negative × Negative | Positive |

Examples:

\[
(-3)(4)=-12
\]

\[
(-3)(-4)=12
\]

Why does negative times negative become positive? One way to understand it is through consistency with distributive arithmetic:

\[
0=(-3)(0)=(-3)(4+(-4))
\]

\[
=(-3)(4)+(-3)(-4)
\]

\[
= -12 + (-3)(-4)
\]

For the total to be zero, the second term must be 12.

### AI connection

A neuron multiplies each input by a weight. A negative weight can reverse the contribution of an input.

---

## 5. Division

Division splits a quantity into equal parts or asks how many groups fit.

\[
12\div3=4
\]

Division by zero is **undefined**:

\[
\frac{5}{0}
\]

There is no number that makes this a valid ordinary division.

### Fractions are division

\[
\frac{3}{4}=3\div4=0.75
\]

### Dividing by a fraction

Dividing by a fraction is equivalent to multiplying by its reciprocal:

\[
6\div\frac{2}{3}=6\times\frac{3}{2}=9
\]

The reciprocal of \(\frac{2}{3}\) is \(\frac{3}{2}\).

---

## 6. Fractions in detail

### Simplifying a fraction

\[
\frac{6}{8}=\frac{3}{4}
\]

We divided both numerator and denominator by 2.

A fraction's value does not change when its numerator and denominator are multiplied or divided by the same nonzero number.

### Adding fractions

If denominators are equal:

\[
\frac{2}{7}+\frac{3}{7}=\frac{5}{7}
\]

If denominators differ, find a common denominator:

\[
\frac{1}{2}+\frac{1}{3}
=\frac{3}{6}+\frac{2}{6}
=\frac{5}{6}
\]

### Multiplying fractions

Multiply numerators and denominators:

\[
\frac{2}{3}\times\frac{4}{5}
=\frac{8}{15}
\]

### AI connection

Neural-network values often appear as decimals such as 0.25 or 0.8. These are simply fractions written in another form.

---

## 7. Decimals and place value

Each decimal position represents a power of ten:

| Position | Value |
|---|---|
| Ones | 1 |
| Tenths | 0.1 |
| Hundredths | 0.01 |
| Thousandths | 0.001 |

For example:

\[
2.347 = 2 + 0.3 + 0.04 + 0.007
\]

### Multiplying decimals

First multiply as if there were no decimal points, then place the decimal based on the total decimal places.

\[
0.2\times0.3=0.06
\]

Since \(0.2=\frac{2}{10}\) and \(0.3=\frac{3}{10}\):

\[
\frac{2}{10}\times\frac{3}{10}=\frac{6}{100}=0.06
\]

### AI connection: scaling

Suppose an input value is 250. A preprocessing step might divide it by 100:

\[
250\div100=2.5
\]

Changing the scale of data can make learning more stable. Later, we will study normalization and standardization.

---

## 8. Order of operations

When an expression contains multiple operations, use this order:

1. Parentheses
2. Exponents and roots
3. Multiplication and division, from left to right
4. Addition and subtraction, from left to right

Example:

\[
3+2\times5
\]

Multiply first:

\[
3+10=13
\]

With parentheses:

\[
(3+2)\times5=5\times5=25
\]

**Important:** Multiplication does not always come before division, and addition does not always come before subtraction. Operations at the same level are evaluated from left to right.

Example:

\[
12\div3\times2=4\times2=8
\]

---

## 9. Powers and roots

A power means repeated multiplication:

\[
2^3=2\times2\times2=8
\]

Here:
- 2 is the base.
- 3 is the exponent.

Examples:

\[
5^2=25, \qquad 10^3=1000
\]

A square root reverses squaring:

\[
\sqrt{25}=5
\]

because \(5^2=25\).

### Negative exponents

\[
2^{-3}=\frac{1}{2^3}=\frac{1}{8}
\]

A negative exponent means take the reciprocal; it does not automatically mean the result is negative.

### AI connection

Powers appear in squared-error loss:

\[
(\text{prediction}-\text{target})^2
\]

They also appear in probability, statistics, and many activation-function formulas.

---

## 10. Percentages

A percentage means “out of 100.”

\[
25\%=\frac{25}{100}=0.25
\]

To find 25% of 80:

\[
0.25\times80=20
\]

Percentages are useful for understanding accuracy, error rates, and proportions in datasets.

---

## 11. Worked example: calculate a neuron’s weighted sum

A simple neuron receives two inputs:

\[
x_1=0.5, \qquad x_2=0.2
\]

Its weights are:

\[
w_1=2, \qquad w_2=-3
\]

Its bias is:

\[
b=1
\]

The neuron calculates:

\[
z=w_1x_1+w_2x_2+b
\]

Substitute the values:

\[
z=2(0.5)+(-3)(0.2)+1
\]

Calculate the products:

\[
z=1-0.6+1
\]

Finish:

\[
\boxed{z=1.4}
\]

This is called a **weighted sum plus bias**. It is one of the most important calculations in neural networks.

---

## 12. Common mistakes

- Forgetting the negative sign when multiplying.
- Adding fractions without finding a common denominator.
- Ignoring the order of operations.
- Thinking \(2^{-3}\) means \(-2^3\).
- Dividing by zero.
- Confusing a percentage with its decimal form: 5% is 0.05, not 5.
- Rounding too early in a multi-step calculation.

---

## 13. Practice exercises

Try these without looking at the answers.

### A. Basic arithmetic
1. \(17-25\)
2. \((-6)(-4)\)
3. \((-24)\div6\)
4. \(7+3\times4\)
5. \((7+3)\times4\)

### B. Fractions and decimals
6. Simplify \(\frac{12}{18}\).
7. Calculate \(\frac{1}{4}+\frac{1}{2}\).
8. Calculate \(\frac{2}{3}\times\frac{3}{5}\).
9. Write 0.75 as a fraction in simplest form.
10. Find 15% of 200.

### C. Powers
11. Calculate \(3^3\).
12. Calculate \(10^{-2}\).
13. Calculate \(\sqrt{81}\).

### D. AI connection
14. Calculate \(z=3(0.4)+2(0.1)-1\).
15. A prediction is 7.5 and the target is 9. Calculate prediction minus target.
16. A data value is 800. Divide it by 100 to scale it.

## Answers

1. -8
2. 24
3. -4
4. 19
5. 40
6. \(\frac{2}{3}\)
7. \(\frac{3}{4}\)
8. \(\frac{2}{5}\)
9. \(\frac{3}{4}\)
10. 30
11. 27
12. 0.01
13. 9
14. \(1.2+0.2-1=0.4\)
15. \(7.5-9=-1.5\)
16. 8

---

## What comes next?

**Lesson 2 — Variables, expressions, and equations**

You will learn what symbols like \(x\), \(w\), and \(b\) mean, how to simplify expressions, and how to solve equations. These are essential for understanding neural-network formulas.
