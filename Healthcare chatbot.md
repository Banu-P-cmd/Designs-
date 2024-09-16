# Designs-
Simplified version of my projects designs

```mermaid

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

    style B fill:#f9f,stroke:#333,stroke-width:4px
