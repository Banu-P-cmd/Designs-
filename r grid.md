graph TD
    A[Client] -->|HTTP Request| B[Flask App]
    B -->|Load Models| C[Pre-trained Models]
    C -->|Model| D[Logistic Regression]
    C -->|Vectorizer| E[TF-IDF Vectorizer]
    C -->|Encoder| F[Label Encoder]
    B -->|Preprocess| G[Text Processing]
    B -->|Predict| D
    D -->|Raw Prediction| F
    F -->|Condition Label| B
    B -->|JSON Response| A
    H[train.py] -->|Train and Save| C
    I[test.py] -->|Test| B
