# Designs-
Simplified version of my projects designs

```mermaid

    graph TD
    A[Structured Data Input] -->|1| B[Anomaly Detection Module<br/>Isolation Forest]
    F[Unstructured Data Input] -->|2| G[Feature Extraction]
    G -->|3| H[Unstructured Data Features]
    B -->|4| C[Anomalies with Scores]
    C -->|5| I[Structured Feature Extraction]
    I -->|6| J[Structured Data Features]
    J -->|7a| K[Feature Combiner]
    H -->|7b| K
    K -->|8| L[Threat Classification Module<br/>RLAIF Neural Network]
    L -->|9| M[Threat Assessments]
    M -->|10| N[Summary Generation Module<br/>T5 Model]
    N -->|11| O[Explanations and Summaries]
    M -->|12a| P[Feedback Mechanism]
    O -->|12b| P
    P -->|13| Q[Weak Supervision Module]
    Q -->|14a| L
    Q -->|14b| N
    P -->|15| R[Reinforcement Learning Module]
    R -->|16| S{Update Components}
    S -->|17a| T[Update Threat Classification]
    S -->|17b| U[Update Summary Generation]
    S -->|17c| V[Enhance Weak Supervision]
    T -->|18| L
    U -->|19| N
    V -->|20| Q

    classDef dataInput fill:#e0f7fa,stroke:#00838f,stroke-width:1px;
    classDef processing fill:#e8eaf6,stroke:#1a237e,stroke-width:1px;
    classDef feedback fill:#fff3e0,stroke:#ff6f00,stroke-width:1px;
    classDef update fill:#f3e5f5,stroke:#6a1b9a,stroke-width:1px;
    class A,F dataInput;
    class B,G,I,K,L,N processing;
    class P,Q,R feedback;
    class S,T,U,V update;
