# Linear Algebra Foundations

## Vectors

A vector is an ordered list of numbers.

In machine learning, vectors represent:

- Tokens
- Embeddings
- Latent variables
- Hidden states
- Features

## Matrices

A matrix is a rectangular array of numbers.

Matrices represent:

- Linear transformations
- Neural network weights
- Attention projections
- Covariance matrices

## Dot Product

```math
a \cdot b = \sum_i a_i b_i
```

The dot product measures alignment between vectors.

## Matrix Multiplication

```math
Y = XW
```

This is the core operation in neural networks.

## Eigenvalues and Eigenvectors

For a matrix `A`:

```math
Av = \lambda v
```

where:

- `v` = eigenvector
- `lambda` = eigenvalue

These matter in PCA, covariance analysis, dynamical systems, and state-space models.

## Covariance Matrix

A covariance matrix describes how dimensions vary together.

In a Gaussian:

```math
\mathcal{N}(\mu, \Sigma)
```

`Sigma` is the covariance matrix.

## Why Linear Algebra Matters

Generative AI is built from vector spaces and matrix operations.

Examples:

- Token embeddings
- Attention
- Latent spaces
- Gaussian distributions
- State-space dynamics
