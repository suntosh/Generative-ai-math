# Generative Adversarial Networks

## Abbreviation

**GAN = Generative Adversarial Network**

## One-Line Definition

A GAN is a generative model where a generator and discriminator are trained against each other.

## Architecture

A GAN has two neural networks:

1. Generator
2. Discriminator

## Generator

The generator takes random noise:

```math
z \sim p(z)
```

and produces a fake sample:

```math
G(z)
```

## Discriminator

The discriminator receives a sample and predicts whether it is real or fake.

```math
D(x)
```

## Training Game

The discriminator tries to distinguish real data from generated data.

The generator tries to fool the discriminator.

The classic GAN objective is:

```math
\min_G \max_D
\mathbb{E}_{x \sim p_{data}}[\log D(x)]
+
\mathbb{E}_{z \sim p(z)}[\log(1 - D(G(z))]
```

## Intuition

The system works like a counterfeiter and detective:

- Generator = counterfeiter
- Discriminator = detective

As the detective improves, the counterfeiter must improve.

## Strengths

- Can generate sharp, realistic samples
- Fast inference after training
- Historically important in image generation

## Weaknesses

- Training instability
- Mode collapse
- Sensitive to hyperparameters
- Hard to evaluate
- Generator may exploit discriminator weaknesses

## Mode Collapse

Mode collapse happens when the generator produces limited varieties of outputs.

Example:

A face generator produces the same kind of face repeatedly instead of covering the full data distribution.

## Why GANs Matter

GANs were a major breakthrough in neural generative modeling and shaped modern thinking about adversarial training.

They are less dominant than diffusion models in many frontier image systems, but remain important historically and conceptually.
