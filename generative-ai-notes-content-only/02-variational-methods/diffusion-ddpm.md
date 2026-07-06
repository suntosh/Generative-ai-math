# Diffusion Models and DDPMs

## Abbreviation

**DDPM = Denoising Diffusion Probabilistic Model**

## One-Line Definition

A diffusion model generates data by learning to reverse a gradual noising process.

## Core Idea

Diffusion models have two processes:

1. Forward process: add noise to data
2. Reverse process: learn to remove noise

## Forward Process

Starting with clean data:

```math
x_0
```

noise is gradually added:

```math
x_0 \rightarrow x_1 \rightarrow x_2 \rightarrow \dots \rightarrow x_T
```

At the final step, the sample is nearly pure noise:

```math
x_T \approx \mathcal{N}(0, I)
```

## Reverse Process

The model learns to denoise step by step:

```math
x_T \rightarrow x_{T-1} \rightarrow \dots \rightarrow x_0
```

## Training Objective

A common DDPM objective trains a neural network to predict the noise added to the sample.

```math
\epsilon_\theta(x_t, t)
```

The loss is often:

```math
\mathcal{L}
=
\mathbb{E}_{x_0, \epsilon, t}
\left[
\|\epsilon - \epsilon_\theta(x_t, t)\|^2
\right]
```

where:

- `epsilon` = true noise
- `epsilon_theta` = predicted noise
- `t` = timestep

## Sampling

To generate a new sample:

1. Start with random noise:

```math
x_T \sim \mathcal{N}(0, I)
```

2. Apply learned denoising steps until reaching:

```math
x_0
```

## Why Diffusion Models Became Important

Diffusion models are highly effective for:

- Image generation
- Audio generation
- Video generation
- Multimodal generation
- Image editing and inpainting

## Strengths

- High-quality samples
- Stable training
- Good mode coverage
- Strong controllability with conditioning

## Weaknesses

- Sampling can be slow
- Requires many denoising steps unless accelerated
- Computationally expensive

## DDPM vs GAN

| Feature | DDPM | GAN |
|---|---|---|
| Training stability | High | Often unstable |
| Sampling speed | Slower | Fast |
| Image quality | Very high | Very high |
| Mode collapse | Less common | Common risk |
| Likelihood foundation | Stronger | Weaker |

## Key Takeaway

Diffusion models dominate many modern image and video generation systems because they combine high sample quality with stable training.
