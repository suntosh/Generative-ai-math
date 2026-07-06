# Transformer-Based Language Models

## Abbreviation

**LM = Language Model**

## One-Line Definition

A transformer-based language model predicts the next token using self-attention over previous tokens.

## Language Modeling Objective

Given tokens:

```math
x_1, x_2, \dots, x_t
```

the model learns:

```math
p(x_t \mid x_{<t})
```

For the full sequence:

```math
p(x) = \prod_{t=1}^{T} p(x_t \mid x_{<t})
```

## Tokenization

Text is split into tokens.

Tokens may be:

- Words
- Subwords
- Characters
- Byte-level units

Example:

```text
Generative AI is powerful
```

might become:

```text
["Gener", "ative", " AI", " is", " powerful"]
```

## Transformer Core Components

### Embeddings

Tokens are converted into vectors.

### Positional Encoding

Because attention does not inherently know order, position information is added.

### Self-Attention

Each token attends to other tokens in the context.

### Causal Masking

In auto-regressive language models, a token can only attend to previous tokens, not future ones.

### Feed-Forward Network

Each transformer block includes an MLP applied to each token representation.

### Layer Normalization and Residual Connections

Used for stable deep network training.

## Training

Training uses next-token prediction with cross-entropy loss.

```math
\mathcal{L}
=
-\sum_{t=1}^{T} \log p(x_t \mid x_{<t})
```

## Inference

At inference time:

1. Provide a prompt.
2. Model predicts probability distribution over next token.
3. Select a token using decoding strategy.
4. Append token.
5. Repeat.

## Decoding Strategies

- Greedy decoding
- Beam search
- Temperature sampling
- Top-k sampling
- Top-p / nucleus sampling

## Strengths

- Excellent for language and code
- Scales with data and compute
- Supports instruction following
- Can be extended to multimodal systems
- Strong ecosystem and tooling

## Weaknesses

- Attention cost grows with context length
- Generation is sequential
- Long-context inference can be expensive
- May hallucinate when uncertain
- Requires alignment and safety layers for production use

## Examples

- GPT-style models
- Claude-style models
- Llama-style models
- Gemini-style models

## Key Takeaway

Transformer-based language models are the dominant architecture for modern text generation and reasoning systems.
