# Neural Network Overview

```mermaid
flowchart LR
    subgraph input[Input Layer]
        I1[x₁]
        I2[x₂]
        I3[x₃]
    end

    subgraph hidden[Hidden Layer(s)]
        H1
        H2
        H3
    end

    subgraph output[Output Layer]
        O1[ŷ]
    end

    I1 --> H1
    I1 --> H2
    I1 --> H3
    I2 --> H1
    I2 --> H2
    I2 --> H3
    I3 --> H1
    I3 --> H2
    I3 --> H3

    H1 --> O1
    H2 --> O1
    H3 --> O1
```

**Description:**  
A feedforward neural network: input units connect to hidden units (with weights and activations), which connect to output units. Each connection has a learnable weight; training adjusts these weights to fit the data.

**Flow:** Input layer → Hidden layer(s) → Output layer. Data flows forward; gradients flow backward during training (backpropagation).
