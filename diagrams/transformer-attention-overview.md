# Transformer: Attention Overview

```mermaid
flowchart TD
    A[Input Tokens] --> B[Token Embeddings]
    B --> C[Positional Encoding]
    C --> D[Multi-Head Self-Attention]
    D --> E[Add & Norm]
    E --> F[Feed-Forward Network]
    F --> G[Add & Norm]
    G --> H[Output / Next Layer]

    D -.-> I[Scaled Dot-Product Attention]
```

**Description:**  
Transformers process sequences in parallel using self-attention to weigh relationships between all tokens, then apply a feed-forward layer per position.

**Key ideas:** No recurrence; attention over full sequence; stack of encoder/decoder blocks.
