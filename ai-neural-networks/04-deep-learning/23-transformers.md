# Lesson 23 — Transformers

Transformers are neural-network architectures built around attention and feed-forward layers. They are widely used for language, vision, and other data.

## Tokens

Text is split into tokens. A token may be a word, part of a word, punctuation, or another text unit.

Each token is mapped to an embedding vector.

## Position information

Attention alone does not automatically know token order. Transformers add positional information so the model can distinguish positions.

## Transformer block

A simplified transformer block contains:
1. Multi-head self-attention.
2. Residual connection.
3. Layer normalization (exact order varies by design).
4. Feed-forward network.
5. Another residual connection and normalization.

## Self-attention

Each token can attend to other tokens in the sequence. This helps capture context.

## Multi-head attention

Multiple attention heads learn different relationships in parallel. Their outputs are combined.

## Feed-forward network

A small neural network is applied independently to each token representation after attention.

## Residual connections

A residual connection adds an input to a transformed result:

`output = input + transformation(input)`

This helps information and gradients flow through deep networks.

## Layer normalization

Layer normalization stabilizes activations by normalizing values within a feature representation, followed by learned scale and shift parameters.

## Decoder-only language models

Many modern text-generation models use decoder-only transformer architectures. They predict the next token based on preceding tokens.

A simplified generation loop:
1. Start with prompt tokens.
2. Compute next-token probabilities.
3. Select a token according to decoding settings.
4. Append token.
5. Repeat.

## Limits

Transformers require substantial data and compute for large-scale training. They can produce incorrect outputs and should not be assumed to know facts reliably.

## Practice

1. What is a token?
2. Why is positional information used?
3. What does a residual connection do?
4. How does a language model generate text?
