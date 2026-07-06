# Exam-Style Questions

## Conceptual

1. Explain why generative modeling can be viewed as learning a probability distribution.
2. Compare VAEs, GANs, and Diffusion Models in terms of training stability and sampling quality.
3. Explain why latent variables are useful in generative modeling.
4. Describe how auto-regressive language models generate text.
5. Explain why state-space models may be more efficient than transformers for long sequences.

## Mathematical

1. Derive the factorization of an auto-regressive sequence model:

```math
p(x) = \prod_{t=1}^{T} p(x_t \mid x_{<t})
```

2. Write the likelihood of a Gaussian Mixture Model.

3. Explain the two terms in the VAE ELBO:

```math
\mathcal{L}_{ELBO}
=
\mathbb{E}_{q(z|x)}[\log p(x|z)]
-
D_{KL}(q(z|x) \parallel p(z))
```

4. Write the basic state-space equations and explain each term.

5. Explain why invertibility is required in flow-based models.

## Applied

1. Which model family would you choose for high-quality image generation and why?
2. Which model family would you choose for code generation and why?
3. Which model family would you consider for very long sequence modeling and why?
4. If a GAN suffers from mode collapse, what is happening?
5. If a diffusion model is too slow at inference, what could be optimized?
