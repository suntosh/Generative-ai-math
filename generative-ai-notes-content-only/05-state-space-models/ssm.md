# State-Space Models

## Abbreviation

**SSM = State-Space Model**

## One-Line Definition

A State-Space Model represents a sequence using a hidden state that evolves over time.

## Basic Form

```math
h_t = A h_{t-1} + B x_t
```

```math
y_t = C h_t + D x_t
```

where:

- `x_t` = input at time `t`
- `h_t` = hidden state
- `y_t` = output
- `A`, `B`, `C`, `D` = model parameters

## Core Intuition

Instead of attending to all previous tokens, an SSM compresses history into a state.

The hidden state carries information forward.

## Classical Uses

State-space models have long been used in:

- Control systems
- Signal processing
- Time-series modeling
- Kalman filters
- Dynamical systems

## Modern Sequence Models

Modern SSM-inspired neural architectures include:

- S4
- Mamba
- Other long-sequence models

## Why SSMs Matter in Generative AI

Transformers are powerful but expensive for long contexts.

Self-attention has significant cost as sequence length grows.

SSMs aim to model long sequences more efficiently by using recurrence/state dynamics.

## Transformer vs SSM

| Feature | Transformer | SSM |
|---|---|---|
| History representation | Attention over tokens | Compressed hidden state |
| Long-context cost | Expensive | More efficient |
| Parallel training | Strong | Architecture-dependent |
| Inference | KV cache grows with context | State can remain compact |

## Strengths

- Efficient long-sequence modeling
- Natural fit for signals and time series
- Potentially lower memory footprint during inference
- Strong alternative to attention for some workloads

## Weaknesses

- Less universally dominant than transformers
- More complex mathematical machinery
- Model quality depends heavily on architecture design

## Key Takeaway

State-Space Models are important because they challenge the assumption that attention is the only path to powerful sequence modeling.
