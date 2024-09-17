
# Designs-
Simplified version of my projects designs

```mermaid

%%{init: {'theme': 'dark', 'themeVariables': { 'primaryColor': '#ff9800', 'lineColor': '#a0a0a0', 'textColor': '#f0f0f0'}}}%%
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
    J -->|Update PBNN| C
    J -->|Update Causal Model| D
    J -->|Update Preprocessor| B

    %% Human Feedback Flow
    G -->|Human Feedback| HF[Human Feedback Loop]
    HF -->|Bias and Quality Feedback| H
    HF -->|Model Performance Evaluation| J

    subgraph "Recommendation Engine Core"
    C
    D
    E
    end

    subgraph "Feedback Loop System"
    H
    I
    J
    HF
    end

    classDef default fill:#2d2d2d,stroke:#c0c0c0,stroke-width:2px,color:#f0f0f0;
    classDef core fill:#4a148c,stroke:#7c4dff,stroke-width:2px,color:#e1bee7;
    classDef feedback fill:#1a237e,stroke:#3f51b5,stroke-width:2px,color:#c5cae9;
    classDef input fill:#1b5e20,stroke:#4caf50,stroke-width:2px,color:#c8e6c9;
    classDef output fill:#b71c1c,stroke:#f44336,stroke-width:2px,color:#ffcdd2;

    class A input;
    class C,D,E core;
    class H,I,J,HF feedback;
    class F output;



    
   
