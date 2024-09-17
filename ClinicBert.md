# Designs-
Simplified version of my projects designs

```mermaid

    graph TD
    A[EHR-Scanned Documents] -->|1| B[Image Preprocessing]
    B -->|2| C[Optical Character Recognition OCR]
    C -->|3| D[Named Entity Recognition NER]
    D -->|4| E[Text Preprocessing]
    E -->|5| F[ClinicalBERT Embedding]
    F -->|6| G[Text Classifier Model]
    
    G -->|7| H[Knee OA Classification]
    G -->|8| I[ACL Classification]

    H -->|9| J[Knee OA Evaluation]
    I -->|10| K[ACL Evaluation]

    G -->|11| L[Model Serialization]
    L -->|12| M[Azure ML Service Deployment]
    M -->|13| N[Azure GPU Compute Instance]
    N -->|14| O[API Endpoint for Predictions]

    subgraph "Azure ML Deployment"
    L
    M
    N
    O
    end

    classDef input fill:#4caf50,stroke:#81c784,stroke-width:2px,color:#ffffff;
    classDef processing fill:#2196f3,stroke:#64b5f6,stroke-width:2px,color:#ffffff;
    classDef classification fill:#ff9800,stroke:#ffb74d,stroke-width:2px,color:#ffffff;
    classDef deployment fill:#e91e63,stroke:#f06292,stroke-width:2px,color:#ffffff;

    class A input;
    class B,C,D,E,F processing;
    class G,H,I,J,K classification;
    class L,M,N,O deployment;
