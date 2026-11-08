# Lesson 20 — Convolutional Neural Networks (CNNs)

CNNs are neural networks designed to use local structure in data, especially images.

## Why ordinary dense layers can be inefficient for images

An image has spatial structure. Nearby pixels often relate to one another. A dense layer treats all pixel positions as independent input positions and may require many parameters.

CNNs use filters that slide across an image.

## Convolution intuition

A small filter (kernel), such as a 3x3 grid, examines a local patch.

At each location:
1. Multiply corresponding image and filter values.
2. Add the products.
3. Add bias (often).
4. Apply activation.
5. Move the filter to another location.

The result is a feature map.

## Shared weights

The same filter weights are reused at different image positions. This reduces parameter count and allows the network to detect a pattern in different locations.

## Channels

An RGB image has three channels:
- red,
- green,
- blue.

A convolution filter typically spans the input channels.

## Padding and stride

- **Stride:** how far the filter moves each step.
- **Padding:** extra border values, often zeros, added around the image.

These affect output dimensions.

## Pooling

Pooling reduces spatial dimensions. Max pooling, for example, takes the largest value in a small region.

## CNN flow

Image → convolution → activation → pooling → more convolution layers → classifier → prediction.

## Practice

1. Why reuse the same filter at many positions?
2. What does stride control?
3. What does max pooling do?
