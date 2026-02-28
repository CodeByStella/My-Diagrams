# ML Data Split: Train, Validation, Test

```mermaid
flowchart TD
    A[Raw Dataset] --> B[Split]
    B --> C[Train Set]
    B --> D[Validation Set]
    B --> E[Test Set]

    C --> F[Model Training]
    D --> G[Hyperparameter Tuning]
    E --> H[Final Evaluation]

    F --> I[Trained Model]
    G -.-> F
    I --> H
```

**Description:**  
Split data into train (fit model), validation (tune hyperparameters, early stopping), and test (unseen holdout for final metrics). Never tune on test.

**Flow:** Raw data → split → train/val/test → train on train set, tune on validation, report on test set.
