# How Embeddings Work in Machine Learning (Discrete Data → Dense Vectors → Model)

```mermaid
flowchart LR
    A[Raw Input<br/>word / item / image / user ID] --> B[Tokenization or Indexing]
    B --> C[Embedding Layer<br/>lookup table]
    C --> D["Dense Vector<br/>e.g. [0.21, -0.44, 0.98, ...]"]
    D --> E[Neural Network / ML Model]
    E --> F[Output<br/>classification / similarity / recommendation]

    C -. learned during training .-> G[(Embedding Matrix Parameters)]
```

**Description:**  
Embeddings convert symbolic or categorical data into dense numeric vectors that machine learning models can understand.

**Flow:**  
Input → Index → Embedding → Vector → Model → Output

**Key Benefits:**

- Compact representation
- Captures semantic similarity
- Trainable parameters
- More efficient than one-hot encoding
