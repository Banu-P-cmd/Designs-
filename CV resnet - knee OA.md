# Designs-
Simplified version of my projects designs

```mermaid
  
graph TD
    A[Start: Pre-trained ResNet-50] --> B[Modify for Medical Imaging]
    B --> C[Fine-tune on Public Medical Dataset]
    C --> D[Company Data Preparation]
    D --> E[MRI Branch: 3D ResNet-18]
    D --> F[X-ray Branch: DenseNet-121]
    E --> G[Fine-tune MRI Branch]
    F --> H[Fine-tune X-ray Branch]
    G --> I[Fusion Network]
    H --> I
    I --> J[Train Fusion Model]
    J --> K[Ensemble Model]
    K --> L[Final OA Grading]
    L --> M[Evaluate on Company Test Set]
    M --> N[Deploy in Clinical Setting]
    N -->|New Data| D
    
    subgraph "Data Flow"
    O[Public Medical Dataset] --> C
    P[Company MRI Data] --> E
    Q[Company X-ray Data] --> F
    R[Paired MRI/X-ray Data] --> I
    end
    
    subgraph "Model Components"
    S[ResNet-50]
    T[3D ResNet-18]
    U[DenseNet-121]
    V[Custom Fusion Network]
    W[Ensemble Model]
    end
