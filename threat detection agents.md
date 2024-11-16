```mermaid

%%{init: {'theme': 'dark', 'themeVariables': { 'primaryColor': '#ff9800', 'lineColor': '#a0a0a0'}}}%%
graph TD
    subgraph Feature_Generation
        F[Unstructured Data Input] -->|1| FF[Adversarial Example<br/>Generation with PGD]
        FF -->|2a| G1[SecureBERT<br/>Security Embeddings]
        F -->|2b| G1
        G1 -->|3| G2[Feature Extraction]
        G2 -->|4| H[Unstructured Data Features]
        A[Structured Data Input] -->|5| AA[Adversarial Data<br/>Generation with PGD]
        AA -->|6a| I1[Structured Feature Extraction]
        A -->|6b| I1
        I1 -->|7| J1[Structured Data Features]
        J1 -->|8| B[Anomaly Detection Module<br/>Isolation Forest]
        B -->|9| C[Anomalies with Scores]
        C -->|10| J[Combined Structured Features]
        H -->|11a| K[Feature Combiner]
        J -->|11b| K
    end
    K -->|12| L[Threat Classification Module<br/>XGBoost + Human Feedback]
    L -->|13| M[Threat Assessments]
    M -->|14| N[Summary Generation Module<br/>T5 Model with PPO]
    N -->|15| O[Explanations and Summaries]
    M -->|16a| P[Feedback Mechanism]
    O -->|16b| P
    P -->|17| Q[Weak Supervision Module]
    Q -->|18a| L
    Q -->|18b| N
    P -->|19| R[Reinforcement Learning Module<br/>PPO for T5]
    R -->|20| S{Update Components}
    S -->|21a| T[Update Threat Classification<br/>XGBoost with Human Feedback]
    S -->|21b| U[Update Summary Generation<br/>T5 with PPO]
    S -->|21c| V[Enhance Weak Supervision]
    S -->|21d| W[Update Isolation Forest]
    S -->|21e| SB[Update SecureBERT]
    S -->|21f| UA[Update Adversarial<br/>Generation Parameters]
    T -->|22| L
    U -->|23| N
    V -->|24| Q
    W -->|25| B
    SB -->|26| G1
    UA -->|27a| AA
    UA -->|27b| FF
    %% Human Feedback Loop
    L -->|Human Feedback| HL[Human Feedback Loop]
    HL -->|Adjust| T
    N -->|Summary Feedback| HL
    R -->|RL Updates| T
    R -->|RL Updates| U
    HL -->|Adjust| U
    %% Model Performance Feedback
    L -->|Detection Results| UA
    classDef dataInput fill:#4caf50,stroke:#81c784,stroke-width:2px;
    classDef processing fill:#2196f3,stroke:#64b5f6,stroke-width:2px;
    classDef feedback fill:#ff9800,stroke:#ffb74d,stroke-width:2px;
    classDef update fill:#e91e63,stroke:#f06292,stroke-width:2px;
    classDef pgd fill:#9c27b0,stroke:#ba68c8,stroke-width:2px;
    class A,F dataInput;
    class B,G1,G2,I1,K,L,N,C,H,J,J1,M,O processing;
    class P,Q,R feedback;
    class S,T,U,V,W,SB,UA update;
    class AA,FF pgd;
    class HL fill:#ff9800,stroke:#ffb74d,stroke-width:2px;
