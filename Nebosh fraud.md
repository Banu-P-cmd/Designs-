# Designs-
Nebosh fraud
```mermaid

flowchart TD
    A[Data Sources] --> DR[Data Regulation Compliance]
    DR --> B[Data Ingestion & Preprocessing]
    B --> C[Real-time Analysis Engine]
    C --> E[Test Delivery Monitoring]
    C --> F[Student Behavior Analysis]
    C --> G[Affiliate Performance Tracking]
    C --> H[Historical Pattern Analysis]
    C --> J[Anomaly Detection]
    E & F & G & H & J --> K[Risk Scoring Engine]
    K --> L[Decision Engine]
    L --> M[Alert Generation]
    L --> N[Automated Action]
    M --> O[Case Management System]
    N --> P[Block/Flag Certification]
    O --> Q[Human Review]
    P --> R[Feedback Loop]
    Q --> R
    R --> S[Model Update & Optimization]
    S -->|Update Models| C
    S <--> PBI[Power BI Dashboard]
    
    classDef default fill:#2d2d2d,stroke:#c0c0c0,stroke-width:2px,color:#f0f0f0
    classDef input fill:#1b5e20,stroke:#4caf50,stroke-width:2px,color:#c8e6c9
    classDef process fill:#0d47a1,stroke:#2196f3,stroke-width:2px,color:#bbdefb
    classDef decision fill:#b71c1c,stroke:#f44336,stroke-width:2px,color:#ffcdd2
    classDef output fill:#ef6c00,stroke:#ff9800,stroke-width:2px,color:#ffe0b2
    classDef compliance fill:#006064,stroke:#00bcd4,stroke-width:2px,color:#e0f7fa
    classDef analytics fill:#bf360c,stroke:#ff5722,stroke-width:2px,color:#ffccbc
    class A input
    class B,C,E,F,G,H,J,K,R,S process
    class L decision
    class M,N,O,P,Q output
    class DR compliance
    class PBI analytics
