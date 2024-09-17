# Designs-
Simplified version of my projects designs

```mermaid

   %%{init: {'theme': 'dark', 'themeVariables': { 'primaryColor': '#ff9800', 'lineColor': '#a0a0a0', 'textColor': '#f0f0f0'}}}%%
graph TD
    A[Patient Query] --> B[AI Agent]
    B --> Z[Final Response]
    subgraph "AI Agent"
        subgraph "Query Understanding Module"
            C[Search Query Analyzer]
            D[Elastic Search]
            E[SBERT Embedding]
            C --> D
            D --> E
        end
        subgraph "Information Retrieval Module"
            F[RAG System]
            G[Document Ranking]
            H[Cosine Similarity Calculator]
            I[LoRA Fine-Tuning for RAG]
            F --> G
            G --> H
            I --> F
        end
        subgraph "Response Generation Module"
            J[OpenAI GPT API]
            K[Response Formatter]
            L[Clinical Accuracy Checker]
            J --> K
            K --> L
        end
        subgraph "Continuous Learning Module"
            M[Adversarial Data Generator]
            N[Performance Evaluator]
            O[RLAIF Hyperparameter Optimizer]
            M --> N
            N --> O
            O --> M
            O --> I
        end
        E --> F
        H --> J
        L --> M
        O -.-> C
        O -.-> F
    end
    B --> C
    L --> Z

    classDef default fill:#2d2d2d,stroke:#c0c0c0,stroke-width:2px,color:#f0f0f0;
    classDef agent fill:#4a148c,stroke:#7c4dff,stroke-width:4px,color:#e1bee7;
    classDef module fill:#1a237e,stroke:#3f51b5,stroke-width:2px,color:#c5cae9;
    classDef input fill:#1b5e20,stroke:#4caf50,stroke-width:2px,color:#c8e6c9;
    classDef output fill:#b71c1c,stroke:#f44336,stroke-width:2px,color:#ffcdd2;

    class A input;
    class B agent;
    class Z output;
    class C,D,E,F,G,H,I,J,K,L,M,N,O module;
            

    
