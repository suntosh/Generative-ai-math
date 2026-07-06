# Information Theory Foundations

## Entropy

Entropy measures uncertainty in a distribution.

```math
H(p) = -\sum_x p(x)\log p(x)
```

High entropy means high uncertainty.

Low entropy means low uncertainty.

## Cross-Entropy

Cross-entropy measures how well one distribution predicts another.

```math
H(p, q) = -\sum_x p(x)\log q(x)
```

In language modeling, cross-entropy is used for next-token prediction.

## KL Divergence

KL divergence measures how much one distribution differs from another.

```math
D_{KL}(p \parallel q)
=
\sum_x p(x)\log \frac{p(x)}{q(x)}
```

For continuous distributions:

```math
D_{KL}(p \parallel q)
=
\int p(x)\log \frac{p(x)}{q(x)} dx
```

## KL Divergence in VAEs

In VAEs:

```math
D_{KL}(q(z|x) \parallel p(z))
```

penalizes the learned latent posterior if it moves too far from the prior.

## Negative Log-Likelihood

Training often minimizes:

```math
-\log p(x)
```

This is equivalent to maximizing log-likelihood.

## Perplexity

Perplexity is commonly used to evaluate language models.

```math
\text{Perplexity} = e^{\text{cross-entropy}}
```

Lower perplexity usually means better next-token prediction.

## Key Takeaway

Information theory connects probability, compression, uncertainty, and model training objectives.
