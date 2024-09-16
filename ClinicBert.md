# Designs-
Simplified version of my projects designs

```mermaid

    graph TD
    A[EHR-Scanned Documents] --> B[Image Preprocessing]
    B --> C[Optical Character Recognition OCR]
    C --> D[Named Entity Recognition NER]
    D --> E[Text Preprocessing]
    E --> F[ClinicalBERT Embedding]
    F --> G[Text Classifier Model]
    G --> H[Knee OA Classification]
    G --> I[ACL Classification]
    H --> J[Knee OA Evaluation]
    I --> K[ACL Evaluation]
    G --> L[Model Serialization]
    L --> M[Azure ML Service Deployment]
    M --> N[Azure GPU Compute Instance]
    N --> O[API Endpoint for Predictions]

    subgraph "Azure ML Deployment"
    L
    M
    N
    O
    end
