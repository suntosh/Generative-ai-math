# Generative AI Interview Questions

## Probabilistic ML

1. What is the difference between a generative and discriminative model?
2. What does it mean to model `p(x)`?
3. Why do we use log-likelihood instead of likelihood?
4. Explain MLE and MAP.
5. What is posterior inference?

## Latent Variable Models

1. What is a latent variable?
2. Why is `p(z | x)` often hard to compute?
3. What is approximate inference?
4. Give examples of latent variables in GMMs, VAEs, and diffusion models.

## GMM

1. What is a Gaussian Mixture Model?
2. What is the role of the hidden component assignment?
3. Explain the EM algorithm.
4. What are the limitations of GMMs?

## VAE

1. What is a VAE?
2. What are the encoder and decoder?
3. What is the ELBO?
4. Why does a VAE use KL divergence?
5. Explain the reparameterization trick.
6. Why can VAEs produce blurry samples?

## Diffusion Models

1. What is the forward noising process?
2. What does the reverse process learn?
3. What does a DDPM predict during training?
4. Why are diffusion models stable to train?
5. Why can diffusion model sampling be slow?

## GAN

1. What are the generator and discriminator?
2. Explain the minimax objective.
3. What is mode collapse?
4. Why are GANs hard to train?
5. Compare GANs with diffusion models.

## Auto-Regressive Language Models

1. What does auto-regressive mean?
2. How does next-token prediction work?
3. What is causal masking?
4. Why is inference sequential?
5. What are common decoding strategies?

## Transformers

1. What is self-attention?
2. Why do transformers need positional information?
3. What is the difference between encoder-only, decoder-only, and encoder-decoder transformers?
4. Why does attention become expensive for long contexts?
5. What is the role of the KV cache?

## State-Space Models

1. What is a State-Space Model?
2. How does an SSM represent sequence history?
3. Why are SSMs interesting for long-context modeling?
4. Compare SSMs and Transformers.

## Flow-Based Models

1. What is a normalizing flow?
2. Why must flow transformations be invertible?
3. How do flow models compute exact likelihood?
4. Compare flow models with VAEs.
