# Designs-
Nebosh recommender 

```mermaid

   flowchart TD
    A[Input Data] --> DR[Data Regulation Compliance]
    DR --> B[Data Preprocessor]
    B --> C[Collaborative Filtering Model]
    B --> D[Content-Based Filtering Model]
    C & D --> E[Hybrid Recommender System]
    E --> CM[Causal Model]
    CM --> F[Recommendation Generator]
    F --> G1[Student Recommendations]
    F --> G2[Affiliate Recommendations]
    G1 --> AB1[Student A/B Testing]
    G2 --> AB2[Affiliate A/B Testing]
    AB1 --> H1[Student Interaction]
    AB2 --> H2[Affiliate Interaction]
    H1 & H2 --> I[Feedback Collector]
    I --> K[Model Update Manager]
    K <--> PBI[Power BI Dashboard]
    K -->|Update Models| C & D & E & CM
    K -->|Update Preprocessor| B
    K -->|Optimize A/B Tests| AB1 & AB2
    H1 -->|Expert Feedback| EF1[Education Expert Feedback]
    H2 -->|Expert Feedback| EF2[Partnership Expert Feedback]
    EF1 & EF2 --> I

    subgraph "Core Recommender Engine"
    C
    D
    E
    CM
    end

    subgraph "B2C: Student Acquisition"
    G1
    AB1
    H1
    EF1
    end

    subgraph "B2B: Affiliate Acquisition"
    G2
    AB2
    H2
    EF2
    end

    subgraph "Feedback and Optimization"
    I
    K
    PBI
    end

    classDef default fill:#2d2d2d,stroke:#c0c0c0,stroke-width:2px,color:#f0f0f0;
    classDef core fill:#4a148c,stroke:#7c4dff,stroke-width:2px,color:#e1bee7;
    classDef b2c fill:#1a237e,stroke:#3f51b5,stroke-width:2px,color:#c5cae9;
    classDef b2b fill:#b71c1c,stroke:#f44336,stroke-width:2px,color:#ffcdd2;
    classDef feedback fill:#1b5e20,stroke:#4caf50,stroke-width:2px,color:#c8e6c9;
    classDef input fill:#ef6c00,stroke:#ff9800,stroke-width:2px,color:#fff3e0;
    classDef compliance fill:#006064,stroke:#00bcd4,stroke-width:2px,color:#e0f7fa;
    classDef analytics fill:#bf360c,stroke:#ff5722,stroke-width:2px,color:#ffccbc;
    class A input;
    class C,D,E,CM core;
    class G1,AB1,H1,EF1 b2c;
    class G2,AB2,H2,EF2 b2b;
    class I,K feedback;
    class DR compliance;
    class PBI analytics;
    
