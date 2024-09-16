graph TD
    A[Member Health Data] --> B[Data Preprocessor]
    B --> C[Probabilistic Bayesian Neural Network]
    B --> D[Interpretable Causal Inference Model]
    C --> E[Recommendation Generator]
    D --> E
    E --> F[Next-Best Action Recommendation]
    F --> G[Member Interaction]
    G --> H[Feedback Collector]
    H --> I[Bias Detection Module]
    I --> J[Model Update Manager]
    J --> |Update PBNN| C
    J --> |Update Causal Model| D
    J --> |Update Preprocessor| B

    subgraph "Recommendation Engine Core"
    C
    D
    E
    end

    subgraph "Feedback Loop System"
    H
    I
    J
    end

    classDef core fill:#f9f,stroke:#333,stroke-width:2px;
    classDef feedback fill:#fcf,stroke:#333,stroke-width:2px;
    class C,D,E core;
    class H,I,J feedback;
