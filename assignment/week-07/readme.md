# Applied Deep Learning: CNN Concepts

## Student Information

* **Name:** Nisha Naresh
* **Student ID:** 101008896
* **Course:** MBAI 5310G, AI Programming
* **University:** Ontario Tech University
* **Term:** Spring 2026
* **Instructor:** Zahra Atf

## Overview

This assignment is a written conceptual review of convolutional neural networks (CNNs). It answers ten short-answer questions drawn from the assigned reading on image classification, convolution, pooling, validation, and error analysis. The goal is to explain each idea in plain language with a concrete example, rather than to train a model. The deliverable is a single PDF of the answers.

## Topics Covered

The ten questions span the core building blocks of a CNN and the practical workflow around training one:

- Image classification and how it differs from detection and segmentation
- Why dense (fully connected) networks scale poorly on image data
- Convolution and the role of filters / kernels
- Feature maps and what they represent
- Weight sharing and its two main benefits
- The ReLU activation function, including a worked example on `[-3, 0, 2, 5]`
- Max pooling and why it is used
- Reshaping Fashion-MNIST images from `28 x 28` to `28 x 28 x 1`
- The difference between training, validation, and test data
- Overfitting and how to read a high-train / low-validation accuracy gap

## Files

| File | Description |
|------|-------------|
| `Deep_Learning-CNN.pdf` | Final submitted answers to all ten questions |
| `README.md` | This file |

## Key Takeaways

A few ideas thread through the whole assignment:

- **Locality and reuse.** Convolution applies a small filter across the entire image and reuses the same weights everywhere, which keeps the parameter count low and lets a feature be detected wherever it appears.
- **Progressive abstraction.** Early layers detect simple patterns such as edges; stacking layers combines these into more complex shapes.
- **Honest evaluation.** Training, validation, and test sets are separated by how much the model is exposed to each, so the final score reflects performance on genuinely unseen data.
- **Generalization over memorization.** A large gap between training and validation accuracy signals overfitting, which is addressed with more data, dropout, or regularization.

## How to Read

Each answer follows the same shape: a plain-language definition first, then a short deeper explanation, then a concrete example to anchor the idea.

## Reference

Questions are based on the assigned course reading covering image classification, convolutional neural networks, convolution, pooling, validation, and error analysis (MBAI5310G AI Programming, Ontario Tech University).
