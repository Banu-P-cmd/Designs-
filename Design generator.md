```mermaid

graph TD
    A[User] -->|Designs in Figma| B(Figma Design)
    B --> C{LLM}
    D[User's Design Repo] -->|Vector Embeddings| E[RAG System]
    E -->|Relevant Documents| C
    C --> F[React Code Generator]
    F -->|Generated React Code| G[Code Review]
    G -->|Feedback| H[RLHF System]
    H -->|Model Updates| C
