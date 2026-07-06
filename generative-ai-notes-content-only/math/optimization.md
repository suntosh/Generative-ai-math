# Optimization Foundations

## Why Optimization Matters

Generative models are trained by minimizing a loss function or maximizing a probability objective.

Examples:

- Maximize likelihood
- Minimize reconstruction loss
- Minimize denoising error
- Minimize cross-entropy

## Gradient Descent

Gradient descent updates parameters in the direction that reduces loss.

```math
\theta_{t+1}
=
\theta_t
-
\eta \nabla_\theta \mathcal{L}(\theta)
```

where:

- `theta` = parameters
- `eta` = learning rate
- `L` = loss function

## Stochastic Gradient Descent

Instead of using the full dataset, SGD uses minibatches.

This makes large-scale training possible.

## Backpropagation

Backpropagation computes gradients through the computational graph.

It applies the chain rule repeatedly.

## Common Losses in Generative AI

| Model | Loss |
|---|---|
| Language Model | Cross-entropy |
| VAE | Reconstruction + KL divergence |
| DDPM | Noise prediction MSE |
| GAN | Adversarial loss |
| Flow | Negative log-likelihood |

## Key Takeaway

Generative AI training is probabilistic modeling plus large-scale numerical optimization.
