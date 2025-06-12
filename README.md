#  Building a Large Language Model from scratch - exploratory LLM pretraining

This repository explores the complete pipeline of **pretraining a Large Language Model (LLM)** from scratch — starting from raw text to a functional GPT-2 clone trained on *The Great Gatsby*. The project is designed to **demystify each component** of a transformer model and walk through each pretraining step.
This was done as a side project during my internship at IISc Bangalore.
---

## Dataset

We use **The Great Gatsby** in `.pdf` format as our training corpus. The text is preprocessed, cleaned, and tokenized for training.

---

##  Pipeline Overview

The following steps are implemented from scratch:

###  1. **Text Preprocessing**
- Load and clean text from a `.pdf` source.
- Normalize whitespace and handle punctuation.

###  2. **Tokenizer**
- Basic character-level and word-level tokenization.
- Implemented a custom tokenizer for small corpus experimentation.

###  3. **Byte Pair Encoding (BPE)**
- Implemented BPE for subword-level tokenization.
- Constructed a vocabulary from training corpus dynamically.

###  4. **Embeddings**
- **Token Embeddings**: Learnable vectors for each token.
- **Positional Embeddings**: Sinusoidal and learned variants explored.
- Combined into input representations.

###  5. **Attention Mechanism**
- Scaled dot-product attention.
- Implemented multi-head attention with masking.

###  6. **Feedforward Network & LayerNorm**
- Standard MLP block with GELU activation.
- Layer normalization before and after attention and FFN blocks.

###  7. **Transformer Block**
- Combined attention, layernorm, and feedforward networks.
- Residual connections implemented.

###  8. **GPT-2 Clone**
- Stacked transformer blocks to form a decoder-only architecture.
- Used causal attention masking for autoregressive training.
- Supports training and inference.

---

##  Pretraining

The model is trained **from scratch** on the tokenized Gatsby dataset using a standard language modeling loss (CrossEntropy).

### 🔗 Weights Available

Download pretrained weights on Hugging Face:

👉 [Pre Trained weights]([https://huggingface.co/your-model-name](https://huggingface.co/VedantBedi/GPT2_self_pretrained/tree/main) 


---
