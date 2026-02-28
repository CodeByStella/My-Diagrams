# LLM Fine-tuning Pipeline

```mermaid
flowchart TD
    A[Base Model] --> B[Prepared Dataset]
    B --> C[Supervised Fine-tuning / LoRA]
    C --> D[Training Loop]
    D --> E[Validation]
    E --> F{Satisfactory?}
    F -->|No| D
    F -->|Yes| G[Export / Merge]
    G --> H[Deployed Model]
```

**Description:**  
Fine-tuning adapts a pretrained LLM to a task or domain using a labeled dataset; methods like LoRA train only small adapter weights for efficiency.

**Flow:** Base model + dataset → SFT/LoRA → train → validate → export → deploy.
