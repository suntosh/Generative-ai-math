# Auto-Regressive Models

## One-Line Definition

An auto-regressive model generates data one element at a time, conditioning each new element on previous elements.

## Sequence Probability

For a sequence:

```math
x = (x_1, x_2, \dots, x_T)
```

an auto-regressive model factorizes the probability as:

```math
p(x) = \prod_{t=1}^{T} p(x_t \mid x_1, x_2, \dots, x_{t-1})
```

This is often written as:

```math
p(x) = \prod_{t=1}^{T} p(x_t \mid x_{<t})
```

## Core Intuition

Generate one token at a time:

```text
previous tokens -> predict next token -> append token -> repeat
```

## Examples

- Language models
- GPT-style models
- PixelRNN / PixelCNN
- Audio generation models
- Sequence-to-sequence decoders

## Training

For language models, training usually uses next-token prediction.

Given:

```text
The cat sat on the
```

the model learns to predict:

```text
mat
```

## Strengths

- Natural fit for text and code
- Strong likelihood-based training
- Easy to condition on context
- Works well with transformer architectures

## Weaknesses

- Generation is sequential
- Long outputs are slow to decode
- Errors can compound
- Attention-based models become expensive with long context

## Key Takeaway

Modern large language models are usually auto-regressive transformer models trained to predict the next token.
