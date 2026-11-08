# Lesson 18 — Training a Neural Network

Training is the repeated process of making predictions, measuring loss, calculating gradients, and updating parameters.

## Training loop

1. Initialize weights and biases.
2. Select a batch of training examples.
3. Run forward propagation.
4. Calculate loss.
5. Calculate gradients with backpropagation.
6. Update parameters with an optimizer.
7. Repeat for many batches.
8. Evaluate on validation data.

## Epoch

An epoch means the model has processed the entire training dataset once (usually in batches).

Training often uses many epochs.

## Batch size

Batch size is the number of examples processed before one update.

For 1,000 examples and batch size 100, one epoch contains 10 batches (assuming no leftover batch).

## Learning rate

The learning rate determines how far parameters move per update.

- Too small: training can be very slow.
- Too large: training may jump around or diverge.
- Suitable rate: loss often decreases steadily, though not always monotonically.

## Optimizers

### SGD
Uses gradient-based updates, often with momentum.

### Momentum
Uses a running direction based on past gradients to smooth updates.

### Adam
Adapts step sizes for individual parameters using estimates of gradient averages and squared gradients. It is widely used, but not automatically best for every task.

## Weight initialization

Weights should generally not all start at the same value. If neurons start identically, they may learn identical features. Random initialization helps break symmetry.

Biases are often initialized to zero or small values depending on the layer.

## Monitoring training

Track:
- training loss,
- validation loss,
- relevant metrics,
- learning rate,
- training time.

If training loss decreases but validation loss worsens, the model may be overfitting.

## Practice

1. What is an epoch?
2. What is batch size?
3. Name the main steps in one training update.
