# Lesson 1 — Numbers and arithmetic: the foundation of AI mathematics

> **Goal:** Learn the number operations that every neural network uses.

## A note about equations

This lesson uses plain-text math so it displays clearly on GitHub, mobile screens, and other Markdown viewers.

- `*` means multiply.
- `/` means divide.
- `**` means “raised to the power.”
- `sqrt(x)` means the square root of x.
- `(-3)` means negative three.

For example, `2 * 0.5 + 1` means “two times one-half, then add one.”

## 1. Why arithmetic matters

A neural network is a program that performs calculations. It multiplies input values by weights, adds them together, adds a bias, and then applies a function.

Example:
```text
z = 2.5 * 0.4 + 0.8
  = 1.0 + 0.8
  = 1.8
```

Every operation must be understood because a network performs these calculations many times.

## 2. Types of numbers

- Natural numbers: 1, 2, 3, 4, …
- Whole numbers: 0, 1, 2, 3, …
- Integers: …, -2, -1, 0, 1, 2, …
- Fractions: 1/2, 3/4, 5/8.
- Decimals: 0.5, 0.75, 0.625.
- Real numbers: numbers on the number line, including values such as sqrt(2).

Neural-network weights can be negative. A negative weight changes the direction of an input's influence.

## 3. Addition and subtraction

Addition combines values:
```text
4 + 3 = 7
```

Subtraction finds a difference:
```text
7 - 4 = 3
4 - 7 = -3
```

Adding negative values:
```text
5 + (-2) = 3
-3 + (-4) = -7
-5 + 8 = 3
```

Subtracting a negative is adding its opposite:
```text
7 - (-3) = 7 + 3 = 10
```

**AI example:** If a model predicts 6 and the correct answer is 10:
```text
prediction - target = 6 - 10 = -4
```
The prediction is four units below the target.

## 4. Multiplication

Multiplication scales a value:
```text
3 * 4 = 12
```

Sign rules:
- positive * positive = positive
- negative * positive = negative
- positive * negative = negative
- negative * negative = positive

Examples:
```text
(-3) * 4 = -12
(-3) * (-4) = 12
```

Why is negative times negative positive? Use the distributive rule:
```text
0 = (-3) * (4 + (-4))
  = (-3)*4 + (-3)*(-4)
  = -12 + (-3)*(-4)
```
The second term must equal 12 for the total to be zero.

## 5. Division

```text
12 / 3 = 4
3 / 4 = 0.75
```

Division by zero is undefined. Never divide by zero in ordinary arithmetic.

Dividing by a fraction means multiplying by its reciprocal:
```text
6 / (2/3) = 6 * (3/2) = 9
```

The reciprocal of 2/3 is 3/2.

## 6. Fractions

Simplify by dividing top and bottom by the same nonzero number:
```text
6/8 = 3/4
```

Add fractions with the same denominator:
```text
2/7 + 3/7 = 5/7
```

For different denominators, find a common denominator:
```text
1/2 + 1/3
= 3/6 + 2/6
= 5/6
```

Multiply fractions:
```text
2/3 * 4/5 = 8/15
```

## 7. Decimals and place value

```text
2.347 = 2 + 0.3 + 0.04 + 0.007
```

Multiplying decimals:
```text
0.2 * 0.3 = 0.06
```

Why? 0.2 = 2/10 and 0.3 = 3/10:
```text
(2/10) * (3/10) = 6/100 = 0.06
```

**AI connection:** Scaling a large value:
```text
250 / 100 = 2.5
```
Data preprocessing often changes input scales.

## 8. Order of operations

Use:
1. Parentheses
2. Powers and roots
3. Multiplication and division (left to right)
4. Addition and subtraction (left to right)

Example:
```text
3 + 2 * 5
= 3 + 10
= 13
```

Parentheses change the result:
```text
(3 + 2) * 5
= 5 * 5
= 25
```

Multiplication and division have equal priority:
```text
12 / 3 * 2 = 4 * 2 = 8
```

## 9. Powers and roots

A power is repeated multiplication:
```text
2**3 = 2 * 2 * 2 = 8
5**2 = 25
```

A square root reverses squaring:
```text
sqrt(25) = 5
```

Negative exponent:
```text
2**(-3) = 1/(2**3) = 1/8 = 0.125
```
A negative exponent means reciprocal, not automatically a negative answer.

AI uses powers in squared error:
```text
(prediction - target)**2
```

## 10. Percentages

Percent means “per 100”:
```text
25% = 25/100 = 0.25
```

Find 25% of 80:
```text
0.25 * 80 = 20
```

## 11. Worked neuron-style calculation

Inputs:
```text
x1 = 0.5
x2 = 0.2
```

Weights:
```text
w1 = 2
w2 = -3
bias = 1
```

Weighted sum plus bias:
```text
z = w1*x1 + w2*x2 + bias
  = 2*0.5 + (-3)*0.2 + 1
  = 1 - 0.6 + 1
  = 1.4
```

This is the central calculation of an artificial neuron. Later chapters explain what weights, inputs, and bias mean and how a network learns them.

## 12. Common mistakes

- Forgetting a negative sign.
- Adding fractions without a common denominator.
- Ignoring parentheses.
- Thinking 2**(-3) means -8.
- Dividing by zero.
- Treating 5% as 5 instead of 0.05.
- Rounding too early.

## 13. Practice

Try these before checking the answers.

1. 17 - 25
2. (-6) * (-4)
3. (-24) / 6
4. 7 + 3 * 4
5. (7 + 3) * 4
6. Simplify 12/18.
7. 1/4 + 1/2
8. 2/3 * 3/5
9. Write 0.75 as a simplified fraction.
10. Find 15% of 200.
11. 3**3
12. 10**(-2)
13. sqrt(81)
14. Calculate z = 3*0.4 + 2*0.1 - 1.
15. Prediction = 7.5, target = 9. Find prediction - target.
16. 800 / 100

### Answers with steps

1. 17 - 25 = -8
2. (-6)*(-4) = 24
3. (-24)/6 = -4
4. 7 + 3*4 = 7 + 12 = 19
5. (7+3)*4 = 10*4 = 40
6. 12/18 = 2/3
7. 1/4 + 1/2 = 1/4 + 2/4 = 3/4
8. (2*3)/(3*5) = 6/15 = 2/5
9. 0.75 = 75/100 = 3/4
10. 0.15*200 = 30
11. 3*3*3 = 27
12. 1/(10*10) = 0.01
13. 9*9 = 81, so sqrt(81)=9
14. 1.2 + 0.2 - 1 = 0.4
15. 7.5 - 9 = -1.5
16. 800/100 = 8

## Next lesson

**Variables, expressions, and equations.** You will learn how symbols such as x, w, and b work, and how to solve the equations used in neural networks.
