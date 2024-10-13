
# Designs-
Simplified version of my projects designs

```mermaid

flowchart TD
    U[User] -->|Input Query/Data| IPA[Input Processing Agent]
    IPA -->|Processed Input| DUA[Data Understanding Agent]
    IPA -->|Processed Input| VPA[Visualization Planning Agent]

    subgraph Data_Processing[Data Processing Subsystem]
        DUA -->|Extracted Information| DEA[Data Extraction Agent]
        DEA -->|Structured Data| DTA[Data Transformation Agent]
        DTA -->|Transformed Data| DQA[Data Quality Agent]
    end

    subgraph Visualization[Visualization Subsystem]
        VPA -->|Visualization Plan| VGA[Visualization Generation Agent]
        VGA -->|Draft Visualization| VEA[Visualization Enhancement Agent]
        VEA -->|Enhanced Visualization| VQA[Visualization Quality Agent]
    end

    DQA -->|Quality-Checked Data| VGA
    VQA -->|Quality-Checked Visualization| PRA[Presentation & Refinement Agent]

    subgraph Interaction[Interaction Subsystem]
        PRA -->|Presented Visualization| UIA[User Interaction Agent]
        UIA -->|User Feedback| FPA[Feedback Processing Agent]
        FPA -->|Processed Feedback| LA[Learning Agent]
    end

    LA -.->|Updates| DUA
    LA -.->|Updates| VPA
    LA -.->|Updates| VGA

    PRA -->|Final Visualization| U

    classDef primary fill:#2196f3,stroke:#1565c0,stroke-width:2px,color:#fff;
    classDef secondary fill:#4caf50,stroke:#2e7d32,stroke-width:2px,color:#fff;
    classDef tertiary fill:#ff9800,stroke:#ef6c00,stroke-width:2px,color:#fff;
    
    class U,IPA,DUA,VPA,PRA,UIA primary;
    class DEA,DTA,DQA,VGA,VEA,VQA secondary;
    class FPA,LA tertiary;
