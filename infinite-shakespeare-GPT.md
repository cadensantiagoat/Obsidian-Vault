---
tags:
  - AI
  - GPT
  - Transformer
status: Completed
deadline:
created: 04/22/2026, 23:06
updated: 04/22/2026, 23:06
---

> [!summary] Project Goal
> *A python script that is a Generative Pretrained Transformer that can display infinite amounts of Shakespeare like text. *

###  Next Actions
- [ ] 

###  Project Notes & Resources
### Project Overview

- **The Goal:** Built a character-level Generative Pretrained Transformer (GPT) from scratch using PyTorch to generate text in the style of Shakespeare.
    
- **The Progression:** Started with a baseline Bigram language model to establish the data pipeline, then upgraded the architecture to a full Decoder-only Transformer.
    
- **The Tech Stack:** Python, PyTorch (specifically `torch.nn`, `torch.optim`, and tensor operations).
    

### Phase 1: Data Pipeline & Baseline (from `shakespear.py`)

- **Tokenization:** Built a custom character-level tokenizer. Read the raw text, extracted all unique characters to form the vocabulary, and created encoding/decoding dictionaries (`stoi` and `itos`) to map characters to integers.
    
- **Data Splitting:** Converted the entire dataset into a 1D PyTorch tensor and split it into training (90%) and validation (10%) sets to evaluate overfitting.
    
- **Batching:** Wrote a `get_batch` function to generate random, independent sequences (context) and their corresponding shifted targets.
    
- **Baseline Bigram Model:** Created a naive model using only an `nn.Embedding` table where the prediction of the next character relies _only_ on the immediate previous character, establishing a baseline loss to beat.
    

### Phase 2: The Transformer Architecture (from `bigram.py`)

- **Token & Positional Embeddings:** Transitioned from a simple lookup table to using both token embeddings and positional embeddings, allowing the model to understand not just the characters, but their specific positions in the sequence.
    
- **Self-Attention Mechanism:** Implemented scaled dot-product attention from scratch. Created Query, Key, and Value linear transformations.
    
- **Autoregressive Masking:** Applied a lower-triangular mask (`tril`) to the attention scores to ensure the model only attends to past context and cannot "look ahead" into the future when predicting the next token.
    
- **Multi-Head Attention:** Scaled the single attention head into multiple parallel heads (`MultiHeadAttention`), allowing the model to focus on different communicative aspects of the sequence simultaneously, followed by a linear projection.
    
- **Transformer Blocks:** Built the core `Block` module combining communication (Multi-Head Attention) and computation (a FeedForward network).
    
- **Optimization via Residuals & Norms:** Added residual (skip) connections and Layer Normalization (`LayerNorm`) to stabilize training and help gradients flow through the deep network.
    

### Phase 3: Training & Generation

- **Training Loop:** Used the `AdamW` optimizer and Cross-Entropy loss to train the model.
    
- **Evaluation:** Implemented a `@torch.no_grad()` evaluation function (`estimate_loss`) to periodically calculate the average loss over multiple batches, ensuring a less noisy estimate of train and validation performance.
    
- **Autoregressive Generation:** Wrote a `generate` function that takes a starting context, predicts the logits for the next token, converts them to probabilities via Softmax, samples the next token using `torch.multinomial`, and appends it to the sequence in a loop.
    

### How to frame this in an interview

- **Focus on the "Why":** Be prepared to explain _why_ the lower-triangular mask is necessary (it prevents data leakage during training) and _why_ positional embeddings are needed (because self-attention has no inherent sense of order or space).
    
- **Acknowledge the scale:** Note that your model operates at the character level and is quite small (a few million parameters) compared to modern LLMs which operate on sub-words (like Byte-Pair Encoding) and have billions of parameters, but the fundamental math in the Transformer blocks is nearly identical.
    
- **Highlight PyTorch skills:** Emphasize your hands-on experience manipulating tensor shapes (`B, T, C` for Batch, Time, Channel/Embedding), managing device placement (CPU vs. GPU/CUDA), and writing custom `nn.Module` classes.