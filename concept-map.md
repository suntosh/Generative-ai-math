# Concept Map

```text
Generative AI
│
├── Probabilistic Machine Learning
│   ├── Probability distributions
│   ├── Likelihood
│   ├── Maximum likelihood estimation
│   ├── Bayesian thinking
│   └── Sampling
│
├── Latent Variable Models
│   ├── Hidden variables
│   ├── Posterior inference
│   ├── Approximate inference
│   └── Variational inference
│
├── Variational Methods
│   ├── Gaussian Mixture Models
│   │   └── EM algorithm
│   ├── Variational Autoencoders
│   │   ├── Encoder
│   │   ├── Decoder
│   │   ├── Reconstruction loss
│   │   └── KL divergence
│   └── Diffusion Models
│       ├── Forward noising process
│       ├── Reverse denoising process
│       └── DDPM
│
├── Adversarial Models
│   └── Generative Adversarial Networks
│       ├── Generator
│       ├── Discriminator
│       ├── Minimax game
│       └── Mode collapse
│
├── Auto-Regressive Models
│   └── Transformer-Based Language Models
│       ├── Tokenization
│       ├── Self-attention
│       ├── Causal masking
│       ├── Next-token prediction
│       └── Decoding
│
├── State-Space Models
│   ├── Hidden state dynamics
│   ├── Long sequence modeling
│   ├── S4
│   └── Mamba
│
└── Flow-Based Models
    ├── Invertible transformations
    ├── Exact likelihood
    ├── Change of variables
    ├── RealNVP
    └── Glow
```

## Big Picture

The major families differ mainly in **how they model and sample from the data distribution**.

| Family | Core Mechanism | Typical Strength |
|---|---|---|
| GMM | Mixture of Gaussians | Simple probabilistic clustering |
| VAE | Latent variables + variational inference | Smooth latent space |
| Diffusion | Reverse a noising process | High-quality images/audio/video |
| GAN | Generator vs discriminator | Sharp samples |
| Auto-Regressive LM | Predict next token | Text, code, reasoning |
| SSM | Evolving hidden state | Efficient long-sequence modeling |
| Flow | Invertible transformations | Exact likelihood |
