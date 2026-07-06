# Variational Autoencoders

## Abbreviation

**VAE = Variational Autoencoder**

## One-Line Definition

A Variational Autoencoder is a latent-variable generative model that learns to encode data into a probabilistic latent space and decode samples back into data.

## Architecture

A VAE has two main components:

1. Encoder
2. Decoder

## Encoder

The encoder maps an input `x` to a latent distribution:

```math
q(z \mid x)
```

Instead of outputting a single latent vector, the encoder usually outputs parameters of a distribution:

```math
\mu(x), \sigma(x)
```

## Decoder

The decoder maps latent variable `z` back to data:

```math
p(x \mid z)
```

## Prior

The latent prior is usually a standard normal distribution:

```math
p(z) = \mathcal{N}(0, I)
```

## Training Objective

The VAE maximizes the ELBO:

```math
\mathcal{L}_{ELBO}
=
\mathbb{E}_{q(z|x)}[\log p(x|z)]
-
D_{KL}(q(z|x) \parallel p(z))
```

## Loss Terms

### Reconstruction Loss

Ensures the generated output resembles the input.

### KL Divergence Loss

Regularizes the latent distribution so that it stays close to the prior.

```math
D_{KL}(q(z|x) \parallel p(z))
```

## Reparameterization Trick

To train with gradient descent, VAEs use the reparameterization trick:

```math
z = \mu + \sigma \odot \epsilon
```

where:

```math
\epsilon \sim \mathcal{N}(0, I)
```

This allows sampling while preserving differentiability.

## Sampling

After training:

1. Sample latent vector:

```math
z \sim \mathcal{N}(0, I)
```

2. Decode:

```math
x \sim p(x \mid z)
```

## Strengths

- Learns smooth latent spaces
- Principled probabilistic foundation
- Useful for representation learning
- Enables interpolation in latent space

## Weaknesses

- Generated images can be blurry
- Likelihood assumptions may be simplistic
- Less visually sharp than GANs and diffusion models

## Key Takeaway

VAEs are foundational because they connect neural networks, latent variables, variational inference, and generative modeling.
