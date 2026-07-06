# Introduction to Probabilistic Machine Learning

## One-Line Definition

Probabilistic Machine Learning models uncertainty explicitly using probability distributions.

## Why It Matters for Generative AI

Generative AI is fundamentally about learning a data distribution and sampling from it.

Instead of only predicting labels, a generative model tries to model:

```math
p(x)
```

or, in conditional generation:

```math
p(x \mid c)
```

where:

- `x` = generated object
- `c` = condition, such as a prompt or label

## Discriminative vs Generative Modeling

### Discriminative Model

Learns:

```math
p(y \mid x)
```

Example:

> Given an image, predict whether it is a cat or dog.

### Generative Model

Learns:

```math
p(x)
```

or:

```math
p(x, y)
```

Example:

> Learn the distribution of cat images and generate a new cat image.

## Core Concepts

### Probability Distribution

A function that assigns probability to possible outcomes.

For continuous data, this is often a density:

```math
p(x)
```

### Likelihood

The probability of the observed data under a model.

Given model parameters `theta`:

```math
p(x \mid \theta)
```

### Log-Likelihood

Instead of maximizing likelihood directly, we usually maximize log-likelihood:

```math
\log p(x \mid \theta)
```

This is numerically more stable and turns products into sums.

### Sampling

Sampling means drawing new examples from the learned distribution.

If a model learns the distribution of images, sampling creates a new image.

## Generative AI Framing

A prompt-based model learns:

```math
p(\text{output} \mid \text{prompt})
```

For a language model:

```math
p(x_t \mid x_1, x_2, \dots, x_{t-1})
```

This is the probability of the next token given the previous tokens.

## Key Takeaway

Generative AI is not just neural networks. It is probability, optimization, representation learning, and sampling combined.
