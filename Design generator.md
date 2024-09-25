```mermaid

flowchart TD
    A[User] -->|Designs in Figma| B[Figma Design]
    B --> C[Computer Vision Model]
    C --> D[Visual Feature Translator]
    D -->|LLM-compatible Design Representation| E{LLM}
    F[User's Design Repo] -->|Vector Embeddings| G[RAG System]
    G -->|Relevant Code Patterns| E
    E --> H[React Code Generator]
    H --> I[Syntax Checker & Optimizer]
    I -->|Optimized React Code| J[Code Review]
    J -->|Feedback| K[RLHF System]
    K -->|Model Updates| E

    subgraph Visual_Features
        L[UI Elements]
        M[Layout]
        N[Colors]
        O[Typography]
        P[Spacing]
        Q[Responsiveness]
    end
    C --> Visual_Features
    Visual_Features --> D

    %% Complexity levels
    classDef low fill:#4CAF50,stroke:#333,color:#fff
    classDef medium fill:#FFC107,stroke:#333,color:#000
    classDef high fill:#FF9800,stroke:#333,color:#000
    classDef veryhigh fill:#F44336,stroke:#333,color:#fff

    class B,F low
    class D,G,I,J medium
    class C,H high
    class E,K veryhigh

    %% Legend
    subgraph Complexity_Legend
        Z1[Low Complexity]:::low
        Z2[Medium Complexity]:::medium
        Z3[High Complexity]:::high
        Z4[Very High Complexity]:::veryhigh
    end
