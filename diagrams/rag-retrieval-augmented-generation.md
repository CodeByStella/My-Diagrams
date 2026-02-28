# RAG: Retrieval Augmented Generation

```mermaid
flowchart TD
    A[User Query] --> B[Query Embedding]
    B --> C[Vector Store / Knowledge Base]
    C --> D[Retrieve Relevant Documents]
    D --> E[Build Augmented Prompt]
    E --> F[LLM]
    F --> G[Generated Response]

    subgraph context
        D
        E
    end
```

**Description:**  
RAG improves LLM answers by retrieving relevant documents and adding them to the prompt, so the model can cite sources and reduce hallucination.

**Flow:**  
Query → Embed → Retrieve → Augment prompt → LLM → Response
