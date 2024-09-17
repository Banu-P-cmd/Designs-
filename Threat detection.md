# Designs-
Simplified version of my projects designs

```mermaid

    graph TD
    A[Structured Data Input] -->|1| B[Anomaly Detection Module]
    F[Unstructured Data Input] -->|2| G[Feature Extraction]
    G -->|3| H[Unstructured Data Features]
    B -->|4| C[Anomalies with Scores]
    C -->|5| D[Weak Supervision Labeling]
    D -->|6| E[Weakly Labeled Anomalies]
    E -->|7| I[Structured Feature Extraction]
    I -->|8| J[Structured Data Features]
    J -->|9| K[Feature Combiner]
    H -->|10| K
    K -->|11| L[Threat Classification Module]
    L -->|12| M[Threat Assessments]
    M -->|13| N[Explanation Generation Module]
    N -->|14| O[Explanations]
    M -->|15| P[Feedback Mechanism]
    O -->|16| P
    P -->|17| Q[Reinforcement Learning Module]
    Q -->|18| R{Update Components}
    R -->|19| S[Update Anomaly Detection]
    R -->|20| T[Update Threat Classification]
    R -->|21| U[Update Explanation Generation]
    R -->|22| V[Enhance Weak Supervision]
    S -->|23| B
    T -->|24| L
    U -->|25| N
    V -->|26| D

    classDef dataInput fill:#e0f7fa,stroke:#00838f,stroke-width:1px;
    classDef processing fill:#e8eaf6,stroke:#1a237e,stroke-width:1px;
    classDef feedback fill:#fff3e0,stroke:#ff6f00,stroke-width:1px;
    classDef update fill:#f3e5f5,stroke:#6a1b9a,stroke-width:1px;
    class A,F dataInput;
    class B,G,D,I,K,L,N processing;
    class P,Q,R feedback;
    class S,T,U,V update;
