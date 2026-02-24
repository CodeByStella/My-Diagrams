# ML Training Pipeline

```mermaid
flowchart TD
    A[Raw Data] --> B[Data Cleaning & Preprocessing]
    B --> C[Feature Engineering / Selection]
    C --> D[Model Selection]
    D --> E[Set Hyperparameters]
    E --> F[Model Training]
    F --> G[Learned Parameters]
    G --> H[Validation / Testing]
    H --> I[Performance Evaluation]
    I -->|Not satisfactory| E
    I -->|Satisfactory| J[Final Trained Model]
```

**Description:** Iterative process: prepare data → choose model & hyperparameters → train → evaluate → tune.

**Notes:** Hyperparameters set _before_ training; parameters learned _during_ training. Loop = hyperparameter tuning. Reflects production ML pipelines.
