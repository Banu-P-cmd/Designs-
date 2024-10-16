# Designs-
Nebosh MMM

```mermaid

flowchart TD
    A[Data Sources] --> B[Data Integration & Preprocessing]
    B --> C[Feature Engineering]
    
    C --> D1[Affiliate Analysis]
    C --> D2[Student Analysis]
    
    D1 --> E1[Affiliate Segmentation]
    D1 --> E2[Affiliate Performance Modeling]
    
    D2 --> F1[Student Segmentation]
    D2 --> F2[Student LTV Prediction]
    
    E1 & E2 & F1 & F2 --> G[Marketing Mix Model]
    
    G --> H1[Channel Attribution]
    G --> H2[Budget Allocation]
    G --> H3[Campaign Optimization]
    
    H1 & H2 & H3 --> I[Recommendation Engine]
    
    I --> J1[Affiliate Recommendations]
    I --> J2[Student Targeting Recommendations]
    
    J1 & J2 --> K[Campaign Execution]
    
    K --> L[Performance Tracking]
    L --> M[Feedback Loop]
    M -->|Update Models| G
    
    B <--> N[Data Governance & Compliance]
    L <--> O[Real-time Dashboards]

    subgraph "Data Analysis"
    D1
    D2
    E1
    E2
    F1
    F2
    end

    subgraph "Decision Making"
    G
    H1
    H2
    H3
    I
    end

    subgraph "Execution & Monitoring"
    K
    L
    M
    O
    end

    classDef default fill:#2d2d2d,stroke:#c0c0c0,stroke-width:2px,color:#f0f0f0;
    classDef input fill:#1b5e20,stroke:#4caf50,stroke-width:2px,color:#c8e6c9;
    classDef process fill:#0d47a1,stroke:#2196f3,stroke-width:2px,color:#bbdefb;
    classDef decision fill:#b71c1c,stroke:#f44336,stroke-width:2px,color:#ffcdd2;
    classDef output fill:#ef6c00,stroke:#ff9800,stroke-width:2px,color:#ffe0b2;
    classDef compliance fill:#006064,stroke:#00bcd4,stroke-width:2px,color:#e0f7fa;
    classDef monitoring fill:#3e2723,stroke:#795548,stroke-width:2px,color:#d7ccc8;
    class A input;
    class B,C,D1,D2,E1,E2,F1,F2 process;
    class G,H1,H2,H3,I decision;
    class J1,J2,K output;
    class N compliance;
    class L,M,O monitoring;
