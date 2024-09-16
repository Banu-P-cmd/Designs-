# Designs-
Simplified version of my projects designs
graph TD
    A[Structured Data Input] --> B[Isolation Forest]
    B --> C{Anomaly Detector}
    C -->|Anomalies| D[Anomaly ID Extractor]
    D --> E[Text Data Retriever]
    F[Unstructured Data Store] --> E
    E --> G[T5 Model]
    G -->|Classification & Summary| H[Feature Combiner]
    C -->|Anomaly Structured Data| I[Structured Feature Extractor]
    I --> H
    J[Additional Structured Data] --> H
    H --> K[RLAIF Neural Network]
    K --> L[Threat Assessment Output]
    L --> M[Feedback Mechanism]
    M --> N[RLAIF Learning Module]
    N --> O{Update Components}
    O --> P[Update RLAIF NN Weights]
    O --> Q[Adjust Isolation Forest Threshold]
    O --> R[Fine-tune T5 Model]
    O --> S[Modify Feature Combination Weights]
    P --> K
    Q --> B
    R --> G
    S --> H

    classDef mainFlow fill:#e1f5fe,stroke:#01579b,stroke-width:2px;
    classDef feedbackFlow fill:#fff8e1,stroke:#ffa000,stroke-width:2px;
    class A,B,C,D,E,F,G,H,I,J,K,L mainFlow;
    class M,N,O,P,Q,R,S feedbackFlow;
