# Variational Methods Overview

## One-Line Definition

Variational methods approximate hard probability distributions with simpler ones that are easier to optimize.

## Why They Are Needed

In many generative models, we want to compute the posterior:

```math
p(z \mid x)
```

But exact computation is often intractable because it requires integrating over all latent variables:

```math
p(x) = \int p(x \mid z)p(z) dz
```

## Core Idea

Approximate the true posterior:

```math
p(z \mid x)
```

with a tractable distribution:

```math
q(z \mid x)
```

Then optimize `q` to be close to the true posterior.

## KL Divergence

The distance between the approximate posterior and the true posterior is often measured using KL divergence:

```math
D_{KL}(q(z \mid x) \parallel p(z \mid x))
```

## ELBO

**Evidence Lower Bound**

The ELBO is an objective used in variational inference.

Instead of directly maximizing:

```math
\log p(x)
```

we maximize a lower bound:

```math
\mathcal{L}_{ELBO}
```

For VAEs, the ELBO commonly appears as:

```math
\mathcal{L}_{ELBO}
=
\mathbb{E}_{q(z|x)}[\log p(x|z)]
-
D_{KL}(q(z|x) \parallel p(z))
```

## Interpretation

The ELBO has two parts:

1. Reconstruction term  
   Measures how well the model reconstructs/generates the data.

2. KL regularization term  
   Keeps the learned latent distribution close to the prior.

## Models in This Family

- Gaussian Mixture Models
- Variational Autoencoders
- Diffusion Models
