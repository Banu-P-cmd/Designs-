# Designs-
Simplified version of my projects designs

```mermaid

    graph TD
    A[Structured Data Input] -->|1| B[Anomaly Detection Module]
    F[Unstructured Data Input] -->|2| G[Feature Extraction]
    G -->|3| H[Unstructured Data Features]
    B -->|4| C[Anomalies with Scores]
    C -->|5| D[Weak Supervision Module]
    D -->|6a| E[Weakly Labeled Anomalies]
    D -->|6b| W[Generated Summaries]
    E -->|7a| I[Structured Feature Extraction]
    W -->|7b| I
    I -->|8| J[Structured Data Features]
    J -->|9a| K[Feature Combiner]
    H -->|9b| K
    W -->|9c| K
    K -->|10| L[Threat Classification Module]
    L -->|11| M[Threat Assessments]
    M -->|12| N[Explanation Generation Module]
    N -->|13| O[Explanations]
    M -->|14| P[Feedback Mechanism]
    O -->|15| P
    P -->|16| Q[Reinforcement Learning Module]
    Q -->|17| R{Update Components}
    R -->|18a| S[Update Anomaly Detection]
    R -->|18b| T[Update Threat Classification]
    R -->|18c| U[Update Explanation Generation]
    R -->|18d| V[Enhance Weak Supervision]
    S -->|19| B
    T -->|20| L
    U -->|21| N
    V -->|22| D

    classDef dataInput fill:#e0f7fa,stroke:#00838f,stroke-width:1px;
    classDef processing fill:#e8eaf6,stroke:#1a237e,stroke-width:1px;
    classDef feedback fill:#fff3e0,stroke:#ff6f00,stroke-width:1px;
    classDef update fill:#f3e5f5,stroke:#6a1b9a,stroke-width:1px;
    class A,F dataInput;
    class B,G,D,I,K,L,N processing;
    class P,Q,R feedback;
    class S,T,U,V update;
    class W processing;
