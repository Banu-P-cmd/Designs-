# Designs-
Simplified version of my projects designs

```mermaid

%%{init: {'theme': 'dark', 'themeVariables': { 'primaryColor': '#ff9800', 'lineColor': '#a0a0a0', 'textColor': '#f0f0f0'}}}%%
%%{init: {'theme': 'dark'}}%%
graph TD
    A[Raw Data] --> B[Feature Extraction]
    B --> C[Causal Model Features]
    B --> D[Additional ML Features]
    
    C --> E[Propensity Score Model<br>Logistic Regression]
    E --> F[Propensity Scores]
    F --> G[Calculate IPTW Weights]
    
    C --> H[IPTW Estimation]
    F --> H
    G --> H
    H --> I[ATE: Estimated Cost Savings]
    
    C --> J[ML Model Input]
    D --> J
    F --> J
    G --> J
    
    J --> K[Feature Engineering]
    K --> L[Derived Features]
    L --> M[Final ML Feature Set]
    
    M --> N[ML Model Training<br>Random Forest]
    N --> O[ML: Predicted Cost Savings]
    
    I --> P{Compare Estimates}
    O --> P
    
    P --> Q[Final Analysis and Insights]
    
    subgraph "Causal Analysis"
    C
    E
    F
    G
    H
    I
    end
    
    subgraph "Machine Learning"
    D
    J
    K
    L
    M
    N
    O
    end
    
    classDef causal fill:#FF6B6B,stroke:#FFD93D,color:#333
    classDef ml fill:#4ECDC4,stroke:#45B7D1,color:#333
    classDef common fill:#F6F6F6,stroke:#FF9F1C,color:#333
    classDef comparison fill:#9B59B6,stroke:#8E44AD,color:#FFF
    class C,E,F,G,H,I causal
    class D,J,K,L,M,N,O ml
    class A,B common
    class P,Q comparison
