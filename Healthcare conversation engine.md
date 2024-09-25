# Designs-
Simplified version of my projects designs

```mermaid

   flowchart TD
    A[Patient] -->|Submits Query| B[AI Agent]
    B --> Z[Final Response]
    subgraph AI_Agent[AI Agent]
        C[Query Analyzer]
        D[Elastic Search]
        E[CBERT Embedding]
        F[RAG System]
        G[Document Ranking with FLAIS]
        I[Fine-Tuning for RAG]
        J[GPT API]
        K[Response Formatter]
        L[Accuracy Checker]
        M[Data Generator]
        N[Evaluator]
        O[RLAIF Optimizer]
        C --> D
        D --> E
        E --> F
        F --> G
        I --> F
        G --> J
        J --> K
        K --> L
        L --> M
        M --> N
        N --> O
        O --> M
        O -.-> C
        O -.-> F
    end
    L --> Z
    %% Complexity levels
    classDef low fill:#4CAF50,stroke:#333,color:#fff
    classDef medium fill:#FFC107,stroke:#333,color:#000
    classDef high fill:#FF9800,stroke:#333,color:#000
    classDef veryhigh fill:#F44336,stroke:#333,color:#fff
    class A,D low
    class C,K,L medium
    class E,F,I,M,N high
    class B,G,J,O veryhigh
    %% Legend
    subgraph Complexity_Legend
        Z1[Low Complexity]:::low
        Z2[Medium Complexity]:::medium
        Z3[High Complexity]:::high
        Z4[Very High Complexity]:::veryhigh
    end
