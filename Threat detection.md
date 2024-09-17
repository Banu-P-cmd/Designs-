# Designs-
Simplified version of my projects designs

```mermaid

   %%{init: {'theme': 'dark', 'themeVariables': { 'primaryColor': '#ff9800', 'lineColor': '#a0a0a0'}}}%%
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
    S -->|17d| W[Update Isolation Forest]
    T -->|18| L
    U -->|19| N
    V -->|20| Q
    W -->|21| B

    classDef dataInput fill:#4caf50,stroke:#81c784,stroke-width:2px,color:#e8f5e9;
    classDef processing fill:#2196f3,stroke:#64b5f6,stroke-width:2px,color:#e3f2fd;
    classDef feedback fill:#ff9800,stroke:#ffb74d,stroke-width:2px,color:#fff3e0;
    classDef update fill:#e91e63,stroke:#f06292,stroke-width:2px,color:#fce4ec;
    class A,F dataInput;
    class B,G,I,K,L,N,C,H,J,M,O processing;
    class P,Q,R feedback;
    class S,T,U,V,W update;
