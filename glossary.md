# Glossary

## AI

**Artificial Intelligence**

A broad field focused on building systems that perform tasks normally associated with human intelligence, such as perception, reasoning, language, planning, and decision-making.

## ML

**Machine Learning**

A subfield of AI where models learn patterns from data instead of being explicitly programmed for every rule.

## Generative AI

A class of AI systems that generate new data, such as text, images, audio, code, video, or structured outputs.

Generative AI models learn a data distribution and sample from it.

## Probabilistic ML

**Probabilistic Machine Learning**

A machine learning framework where uncertainty is modeled explicitly using probability distributions.

## Latent Variable

A hidden variable that is not directly observed but explains structure in the observed data.

Example:

```math
z \rightarrow x
```

where `z` is the hidden cause and `x` is the observed data.

## GMM

**Gaussian Mixture Model**

A probabilistic model that assumes data comes from a mixture of multiple Gaussian distributions.

## EM

**Expectation-Maximization**

An iterative algorithm often used to train latent variable models such as Gaussian Mixture Models.

It alternates between:

1. Estimating hidden assignments
2. Updating model parameters

## VAE

**Variational Autoencoder**

A latent-variable generative model with an encoder and decoder.

The encoder maps data into a latent distribution. The decoder generates data from latent variables.

## KL Divergence

**Kullback-Leibler Divergence**

A measure of how different one probability distribution is from another.

Often written as:

```math
D_{KL}(q(z|x) \parallel p(z))
```

In VAEs, KL divergence regularizes the latent space.

## DDPM

**Denoising Diffusion Probabilistic Model**

A diffusion model trained to reverse a gradual noising process.

It learns to generate data by starting from noise and denoising step by step.

## GAN

**Generative Adversarial Network**

A generative model with two competing neural networks:

- Generator
- Discriminator

The generator creates fake samples. The discriminator tries to distinguish fake samples from real ones.

## LM

**Language Model**

A model that assigns probabilities to sequences of tokens.

Modern LMs are usually trained using next-token prediction.

## Transformer

A neural network architecture based on self-attention.

Transformers are the foundation of most modern large language models.

## Auto-Regressive Model

A model that generates data one step at a time, conditioning each new output on previous outputs.

```math
p(x) = \prod_{t=1}^{T} p(x_t \mid x_{<t})
```

## SSM

**State-Space Model**

A sequence model that represents history using a hidden state that evolves over time.

## Flow-Based Model

A generative model based on invertible transformations.

Flow models allow exact likelihood computation using the change-of-variables formula.

## Normalizing Flow

A flow-based model that transforms a simple probability distribution into a complex one using a sequence of invertible functions.
