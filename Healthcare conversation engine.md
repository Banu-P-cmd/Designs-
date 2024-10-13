# Designs-
Simplified version of my projects designs

```mermaid

   flowchart TD
    A[Patient] -->|Submits Query| QRA[Query Reception Agent]
    QRA --> Z[Final Response]
    
    subgraph Multi_Agent_System[Multi-Agent AI System]
        QRA -->|Forwards Query| QAA[Query Analysis Agent]
        QAA -->|Processed Query| SRA[Search & Retrieval Agent]
        SRA -->|Relevant Documents| RAGA[RAG Agent]
        RAGA -->|Context & Query| LLA[LLM Agent]
        LLA -->|Raw Response| RFA[Response Formatting Agent]
        RFA -->|Formatted Response| ACA[Accuracy Checking Agent]
        ACA -->|Verified Response| QRA
        
        subgraph Search_Retrieval_Agent[Search & Retrieval Agent]
            SRA1[Elastic Search]
            SRA2[CBERT Embedding]
            SRA3[Document Ranking with FLAIS]
            SRA1 --> SRA2 --> SRA3
        end
        
        subgraph RAG_Agent[RAG Agent]
            RAGA1[RAG System]
            RAGA2[Fine-Tuning for RAG]
            RAGA2 --> RAGA1
        end
        
        subgraph LLM_Agent[LLM Agent]
            LLA1[Llama Model]
        end
        
        subgraph Optimization_Agent[Optimization Agent]
            OA1[Data Generator]
            OA2[Evaluator]
            OA3[RLAIF Optimizer]
            OA1 --> OA2 --> OA3
            OA3 --> OA1
        end
        
        ACA -->|Feedback| OA1
        OA3 -.->|Optimizations| QAA
        OA3 -.->|Optimizations| RAGA
        OA3 -.->|Optimizations| LLA
    end
    
    %% Complexity levels
    classDef low fill:#4CAF50,stroke:#333,color:#fff
    classDef medium fill:#FFC107,stroke:#333,color:#000
    classDef high fill:#FF9800,stroke:#333,color:#000
    classDef veryhigh fill:#F44336,stroke:#333,color:#fff
    
    class A,SRA1 low
    class QRA,RFA,ACA medium
    class QAA,SRA2,RAGA1,RAGA2,OA1,OA2 high
    class SRA,RAGA,LLA,SRA3,LLA1,OA3 veryhigh
    
    %% Legend
    subgraph Complexity_Legend
        Z1[Low Complexity]:::low
        Z2[Medium Complexity]:::medium
        Z3[High Complexity]:::high
        Z4[Very High Complexity]:::veryhigh
    end
        
