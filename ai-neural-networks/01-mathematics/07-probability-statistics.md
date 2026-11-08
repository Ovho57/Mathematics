# Lesson 7 — Probability and Statistics

Machine learning uses data, uncertainty, averages, and probability.

## 1. Probability

Probability measures how likely an event is.

It ranges from 0 to 1:
- 0 means impossible.
- 1 means certain.
- 0.5 means a 50% chance.

A fair coin has:

`P(heads)=1/2=0.5`

## 2. Events and outcomes

A die has six equally likely outcomes. The probability of rolling a 4 is:

`P(4)=1/6`

The probability of rolling an even number is:

`P(even)=3/6=1/2`

## 3. Mean (average)

Add values and divide by how many values there are.

For [2,4,6]:

`mean=(2+4+6)/3=12/3=4`

## 4. Median

Sort the values and choose the middle.

For [1,9,3]:

Sorted: [1,3,9]

Median = 3.

For an even number of values, average the two middle values.

## 5. Variance and standard deviation

Variance measures how spread out values are around their mean.

For a population:

`variance = average of (value - mean)^2`

Example: [2,4,6], mean=4.

Squared differences:
- (2-4)^2 = 4
- (4-4)^2 = 0
- (6-4)^2 = 4

Variance:

`(4+0+4)/3 = 8/3`

Standard deviation is the square root of variance.

## 6. Conditional probability

Conditional probability means probability given some information.

`P(A|B)` means “probability of A given B.”

This idea matters when a model estimates a probability based on observed features.

## 7. Softmax intuition

Softmax converts a list of scores into probabilities that sum to 1.

For scores [2,1], softmax is:

`softmax(z_i)=exp(z_i)/sum_j exp(z_j)`

The exponential makes larger scores receive more probability. In practice, software computes softmax carefully to avoid numerical overflow.

## Practice

1. Find the mean of [3,5,7,9].
2. What is the probability of rolling 1 or 2 on a fair six-sided die?
3. If two class probabilities are 0.7 and 0.3, do they sum to 1?

## Answers

1. 6
2. 2/6 = 1/3
3. Yes
