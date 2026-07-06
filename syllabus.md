# Generative AI Syllabus

## 1. Introduction to Probabilistic Machine Learning

Generative AI starts with probabilistic modeling.

A generative model tries to learn the probability distribution that produced the data.

For data `x`, the model learns:

```math
p(x)
```

For conditional generation, the model learns:

```math
p(x \mid c)
```

where:

- `x` = data sample, such as text, image, audio, video, code
- `c` = condition, such as prompt, class label, caption, previous tokens

## 2. Variational Methods and Latent Variable Models

Latent variable models assume observed data is generated from hidden factors.

```math
z \rightarrow x
```

where:

- `z` = latent variable
- `x` = observed data

Topics:

- Gaussian Mixture Models
- Variational Autoencoders
- Diffusion Models / Denoising Diffusion Probabilistic Models

## 3. Adversarial Generative Models

Adversarial models train two networks against each other.

Core model:

- Generative Adversarial Network

## 4. Auto-Regressive Models

Auto-regressive models generate one element at a time.

For a sequence:

```math
x = (x_1, x_2, \dots, x_T)
```

the probability is factorized as:

```math
p(x) = \prod_{t=1}^{T} p(x_t \mid x_1, x_2, \dots, x_{t-1})
```

Topics:

- Transformer-based Language Models
- GPT-style next-token prediction

## 5. State-Space Models

State-Space Models represent sequences using hidden states that evolve over time.

Basic form:

```math
h_t = A h_{t-1} + B x_t
```

```math
y_t = C h_t + D x_t
```

Topics:

- Classical State-Space Models
- Modern sequence models such as S4 and Mamba

## 6. Flow-Based Models

Flow-based models use invertible transformations.

They transform a simple distribution into a complex data distribution.

```math
z \sim \mathcal{N}(0, I)
```

```math
x = f(z)
```

Because `f` is invertible:

```math
z = f^{-1}(x)
```

Topics:

- Normalizing Flows
- NICE
- RealNVP
- Glow
