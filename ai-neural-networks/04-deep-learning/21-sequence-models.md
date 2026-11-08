# Lesson 21 — Recurrent Networks and Sequence Models

Sequence models process data where order matters.

Examples:
- text,
- speech,
- time series,
- sensor readings.

## Why order matters

The sentence “dog bites person” has a different meaning from “person bites dog.” A model needs information about order.

## Recurrent neural networks (RNNs)

An RNN processes a sequence step by step and maintains a hidden state.

A simplified formula:

`h_t = activation(W_x*x_t + W_h*h_(t-1) + b)`

Where:
- x_t is the input at time t,
- h_(t-1) is the previous hidden state,
- h_t is the new hidden state.

The hidden state carries information from earlier steps.

## Challenges

Basic RNNs can struggle with long-range relationships because gradients may vanish or explode during training.

## LSTM and GRU

LSTM and GRU architectures use gates to control information flow and help preserve useful information over longer sequences.

## Transformers

Transformers became very important for sequence processing. Unlike classic recurrent networks, they use attention to relate tokens to one another and can process many positions in parallel during training.

## Practice

1. Why does sequence order matter?
2. What information does an RNN hidden state carry?
3. Name one problem basic RNNs may experience.
