# Likelihood, Maximum Likelihood Estimation, and MAP

## Likelihood

Likelihood measures how well model parameters explain observed data.

Given data:

```math
D = \{x_1, x_2, \dots, x_n\}
```

and parameters `theta`, the likelihood is:

```math
L(\theta) = p(D \mid \theta)
```

Assuming independent samples:

```math
L(\theta) = \prod_{i=1}^{n} p(x_i \mid \theta)
```

## Log-Likelihood

We usually maximize log-likelihood:

```math
\log L(\theta) = \sum_{i=1}^{n} \log p(x_i \mid \theta)
```

## MLE

**Maximum Likelihood Estimation**

MLE chooses parameters that make the observed data most likely:

```math
\theta^* = \arg\max_{\theta} p(D \mid \theta)
```

or:

```math
\theta^* = \arg\max_{\theta} \sum_{i=1}^{n} \log p(x_i \mid \theta)
```

## MAP

**Maximum A Posteriori Estimation**

MAP includes a prior over parameters:

```math
\theta^* = \arg\max_{\theta} p(\theta \mid D)
```

Using Bayes' rule:

```math
p(\theta \mid D) \propto p(D \mid \theta)p(\theta)
```

So:

```math
\theta^* = \arg\max_{\theta} \left[\log p(D \mid \theta) + \log p(\theta)\right]
```

## MLE vs MAP

| Method | Uses Prior? | Objective |
|---|---:|---|
| MLE | No | Maximize likelihood |
| MAP | Yes | Maximize posterior |

## Why This Matters

Most generative models can be viewed as trying to maximize some form of likelihood, approximate likelihood, or likelihood-inspired objective.

Examples:

- GMMs maximize data likelihood using EM.
- VAEs maximize a lower bound on likelihood.
- Diffusion models optimize a denoising objective related to likelihood.
- Language models maximize next-token log-likelihood.
