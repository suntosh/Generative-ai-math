# Latent Variable Models

## One-Line Definition

A latent variable model explains observed data using hidden variables.

## Basic Idea

Observed data often has hidden causes.

For example:

- An image of a face may depend on hidden factors such as identity, pose, lighting, expression, and camera angle.
- A sentence may depend on hidden factors such as topic, style, intent, and domain.

We represent this as:

```math
z \rightarrow x
```

where:

- `z` = latent variable
- `x` = observed data

## Joint Distribution

A typical latent variable model defines:

```math
p(x, z) = p(x \mid z)p(z)
```

where:

- `p(z)` = prior over latent variables
- `p(x | z)` = likelihood or decoder model

## Posterior Inference

Given an observed sample `x`, we often want:

```math
p(z \mid x)
```

This tells us which hidden variables likely produced `x`.

## The Hard Part

For many models, the posterior is intractable:

```math
p(z \mid x) = \frac{p(x \mid z)p(z)}{p(x)}
```

The denominator requires integrating over all possible latent variables:

```math
p(x) = \int p(x \mid z)p(z) dz
```

This is often computationally impossible for complex models.

## Approximate Inference

Because exact inference is hard, we approximate the posterior.

In variational inference, we use a simpler distribution:

```math
q(z \mid x)
```

to approximate:

```math
p(z \mid x)
```

## Examples

| Model | Latent Variable |
|---|---|
| GMM | Cluster/component assignment |
| VAE | Continuous latent representation |
| Diffusion | Noisy intermediate states |
| Topic model | Topic mixture |
| Hidden Markov Model | Hidden state sequence |

## Key Takeaway

Latent variable models are the foundation behind many generative systems because they separate hidden structure from observed data.
