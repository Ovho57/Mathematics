# Lesson 25 — Debugging, Experiments, and Next Steps

## Debugging a neural network

When a model fails, do not randomly change everything. Check one thing at a time.

### Shape errors
Check dimensions:
- input feature count,
- weight matrix shape,
- bias shape,
- output size.

For a dense layer with n inputs and m neurons, W usually has shape n by m when using row-batch inputs in NumPy.

### Loss does not decrease
Possible causes:
- learning rate too high or too low,
- incorrect gradient,
- wrong labels,
- incompatible activation and loss,
- bad data scaling,
- model too small,
- implementation error.

### NaN or infinite values
Possible causes:
- overflow,
- division by zero,
- taking logarithm of zero,
- unstable numerical operations,
- learning rate too large.

### Training good, validation bad
Possible overfitting, leakage, or a mismatch between training and validation data.

## Experiment responsibly

Keep a record:
- model architecture,
- dataset,
- learning rate,
- batch size,
- optimizer,
- epoch count,
- training loss,
- validation metrics.

Change one major factor at a time so you can learn what caused the result.

## Suggested next subjects

- Python fundamentals
- NumPy and tensor shapes
- linear algebra in more depth
- probability and statistics
- calculus and chain rule
- PyTorch or TensorFlow
- CNN image classification
- sequence models and Transformers
- model evaluation and responsible AI

## Final checkpoint

Try explaining, without looking:
1. What a neuron calculates.
2. What weights and biases are.
3. Why layers need activations.
4. What forward propagation does.
5. What loss measures.
6. What backpropagation calculates.
7. What gradient descent changes.
8. Why train/validation/test sets differ.
9. How a transformer uses attention.

If you can explain these concepts and work through small examples, you have built a strong foundation for further AI engineering.
