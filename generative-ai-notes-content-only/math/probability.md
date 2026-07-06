# Probability Foundations

## Random Variable

A random variable represents an uncertain quantity.

Examples:

- Token identity
- Pixel intensity
- Latent vector
- Class label

## Probability Distribution

A distribution assigns probabilities to possible values.

Discrete example:

```math
p(x_i)
```

Continuous example:

```math
p(x)
```

## Conditional Probability

```math
p(x \mid y)
```

This means the probability of `x` given `y`.

In generative AI:

```math
p(\text{answer} \mid \text{prompt})
```

## Joint Probability

```math
p(x, y)
```

The probability of both `x` and `y`.

## Marginal Probability

```math
p(x) = \sum_y p(x, y)
```

or for continuous variables:

```math
p(x) = \int p(x, z) dz
```

## Bayes' Rule

```math
p(z \mid x)
=
\frac{p(x \mid z)p(z)}{p(x)}
```

## Why Bayes' Rule Matters

In latent variable models, we often observe `x` and want to infer hidden cause `z`.

```math
p(z \mid x)
```

This is posterior inference.

## Expectation

```math
\mathbb{E}_{p(x)}[f(x)]
```

The average value of a function under a probability distribution.

## Key Takeaway

Probabilistic ML gives generative AI its mathematical language.
