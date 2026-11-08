# Lesson 22 — Embeddings and Attention

## Embeddings

An embedding maps an item to a vector of numbers.

For example, a word or token may be represented by:

`embedding("cat") = [0.2, -0.1, 0.7, ...]`

Real embeddings can contain hundreds or thousands of values.

The vector is learned or otherwise constructed so that it can be useful to a model. Embedding dimensions do not have simple human-readable meanings by default.

## Similarity

The dot product and cosine similarity can compare vectors.

Cosine similarity:

`cosine(a,b) = (a dot b)/(||a||*||b||)`

It measures the angle-based similarity of two nonzero vectors.

## Attention intuition

Attention lets a model weigh information from different positions.

A token can assign more attention to other tokens that are useful for interpreting it.

## Query, key, value

Attention uses three transformed vectors:
- Query (Q): what this position is looking for.
- Key (K): what a position offers for matching.
- Value (V): information to combine if the position is attended to.

These are learned transformations of the input representations.

## Scaled dot-product attention

`Attention(Q,K,V)=softmax(Q*K^T/sqrt(d_k))*V`

Interpretation:
1. Compare queries and keys using dot products.
2. Divide scores by sqrt(d_k) to control scale.
3. Apply softmax to turn scores into weights.
4. Use weights to combine value vectors.

## Practice

1. What does an embedding represent?
2. What are Q, K, and V used for?
3. What does softmax do to attention scores?
