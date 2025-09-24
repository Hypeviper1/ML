## 🔹 Feature Engineering Overview

```mermaid
flowchart TD
    A[Feature Engineering] --> B1[Feature Transformation]
    A --> B2[Feature Construction]
    A --> B3[Feature Selection]
    A --> B4[Feature Extraction]

    %% Feature Transformation
    B1 --> C1[Missing Value Imputation]
    C1 --> D1[Mean/Median/Mode]
    C1 --> D2[kNN, Regression, MICE]

    B1 --> C2[Categorical Features Encoding]
    C2 --> D3[One-Hot, Ordinal, Label]
    C2 --> D4[Target, Frequency, Hashing]

    B1 --> C3[Outlier Handling]
    C3 --> D5[Z-Score, IQR, Winsorization]
    C3 --> D6[Isolation Forest, DBSCAN]

    B1 --> C4[Feature Scaling]
    C4 --> D7[Standardization, Min-Max]
    C4 --> D8[Robust, MaxAbs, Log, Power]

    %% Feature Construction
    B2 --> C5[Polynomial & Interaction]
    B2 --> C6[Domain-Specific]
    C6 --> D9[Aggregation, Ratios, Lag Features]
    C6 --> D10[Text Features: TF-IDF, Sentiment]

    %% Feature Selection
    B3 --> C7[Filter Methods]
    C7 --> D11[Correlation, Chi-Square, ANOVA]
    B3 --> C8[Wrapper Methods]
    C8 --> D12[RFE, Forward/Backward]
    B3 --> C9[Embedded Methods]
    C9 --> D13[Lasso, Ridge, ElasticNet]
    C9 --> D14[Tree-based Importance]

    %% Feature Extraction
    B4 --> C10[Dimensionality Reduction]
    C10 --> D15[PCA, LDA, ICA, Factor Analysis]
    B4 --> C11[Manifold Learning]
    C11 --> D16[t-SNE, UMAP, Isomap]
    B4 --> C12[Deep Learning Based]
    C12 --> D17[Autoencoders, Embeddings]
