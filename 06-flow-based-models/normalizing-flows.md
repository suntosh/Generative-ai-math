# Flow-Based Models and Normalizing Flows

## One-Line Definition

Flow-based models generate data using invertible transformations from a simple distribution to a complex data distribution.

## Core Idea

Start with a simple latent distribution:

```math
z \sim \mathcal{N}(0, I)
```

Transform it into data:

```math
x = f(z)
```

Because the transformation is invertible:

```math
z = f^{-1}(x)
```

## Normalizing Flow

A normalizing flow is a sequence of invertible transformations:

```math
z_0 \rightarrow z_1 \rightarrow z_2 \rightarrow \dots \rightarrow x
```

Each transformation must be invertible.

## Exact Likelihood

Flow models can compute exact likelihood using the change-of-variables formula.

```math
p_X(x)
=
p_Z(f^{-1}(x))
\left|
\det
\frac{\partial f^{-1}}{\partial x}
\right|
```

## Why Invertibility Matters

Invertibility allows both directions:

### Generation

```math
z \rightarrow x
```

### Density Evaluation

```math
x \rightarrow z
```

This makes flow models mathematically clean.

## Examples

- NICE
- RealNVP
- Glow
- Masked Autoregressive Flow
- Neural Spline Flows

## Strengths

- Exact likelihood
- Efficient sampling and inference
- Strong probabilistic foundation
- Good for density estimation

## Weaknesses

- Invertibility constrains architecture design
- Can be memory-heavy
- Less dominant than diffusion and transformer models for frontier generation

## Flow Models vs VAEs

| Feature | Flow Model | VAE |
|---|---|---|
| Likelihood | Exact | Lower bound |
| Latent mapping | Invertible | Approximate |
| Architecture constraints | High | Lower |
| Sampling | Direct | Direct |
| Reconstruction | Exact-ish through inverse | Learned decoder |

## Key Takeaway

Flow-based models are important because they provide exact likelihood while still allowing complex generative modeling.
