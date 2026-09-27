# transformers-from-scratch

A step-by-step implementation of the original Transformer architecture from scratch using PyTorch.

The goal of this project is to code transformers from scratch by implementing the individual components ourselves instead of relying on high-level Transformer implementations.

The final goal is to build and train an encoder-decoder Transformer for English → French translation.

---

## Project Goal

This project is based on the original Transformer architecture introduced in:

> Vaswani et al., "Attention Is All You Need" (2017)

The implementation is being built incrementally, starting from the Transformer encoder and eventually extending it into a complete encoder-decoder Transformer.

The focus is on understanding:

- Tensor shapes
- Tokenization
- Embeddings
- Positional information
- Query, Key, and Value
- Self-attention
- Multi-head attention
- Residual connections
- Layer normalization
- Feed-forward networks
- Causal masking
- Cross-attention
- Encoder-decoder interaction
- Teacher forcing
- Autoregressive generation
- Transformer training

---

# Current Progress

## Dataset and Preprocessing

- [x] Load OPUS Books dataset
- [x] English-French translation pairs
- [x] Tokenization
- [x] Vocabulary construction
- [x] Special tokens
  - `<PAD>`
  - `<UNK>`
  - `<BOS>`
  - `<EOS>`
- [x] Convert tokens to token IDs
- [x] Padding
- [x] Fixed context length
- [x] PyTorch DataLoader

## Transformer Encoder

- [x] Token embeddings
- [x] Positional embeddings
- [x] Query projections
- [x] Key projections
- [x] Value projections
- [x] Scaled dot-product attention
- [x] Softmax attention weights
- [x] Multi-head self-attention
- [x] Concatenation of attention heads
- [x] Output projection
- [x] Residual connections
- [x] Layer normalization
- [x] Feed-forward network
- [x] Single Transformer encoder block
- [ ] Multiple stacked encoder blocks

## Transformer Decoder

- [ ] Target token embeddings
- [ ] Positional embeddings
- [ ] Masked self-attention
- [ ] Causal masking
- [ ] Decoder residual connections
- [ ] Decoder layer normalization
- [ ] Cross-attention
- [ ] Decoder feed-forward network
- [ ] Decoder output projection
- [ ] Autoregressive decoding

## Complete Transformer

- [ ] Complete encoder-decoder architecture
- [ ] Encoder → decoder data flow
- [ ] Padding masks
- [ ] Causal masks
- [ ] Teacher forcing
- [ ] Cross-entropy loss
- [ ] Training loop
- [ ] Model evaluation
- [ ] Model saving and loading

## Translation

- [ ] Train Transformer on OPUS Books
- [ ] English → French translation
- [ ] Autoregressive generation
- [ ] Evaluate generated translations
- [ ] Experiment with model hyperparameters

---

# Architecture

The current implementation contains a Transformer encoder block.

```text
Input Tokens
     │
     ▼
Token Embeddings
     │
     +
Positional Embeddings
     │
     ▼
Encoder Block
     │
     ├── Multi-Head Self-Attention
     │
     ├── Residual Connection
     │
     ├── Layer Normalization
     │
     ├── Feed-Forward Network
     │
     ├── Residual Connection
     │
     └── Layer Normalization
     │
     ▼
Encoder Output
