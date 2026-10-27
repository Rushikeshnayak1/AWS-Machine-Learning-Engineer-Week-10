# Conceptual workflow diagrams by presentation

## Part 1 — Data Wrangler
```mermaid
flowchart LR
    A[Connect to source] --> B[Preview and profile]
    B --> C[Transform data / features]
    C --> D[Quick Model: early feedback]
    C --> E[Export reusable flow]
    E --> F[Processing / pipeline]
```

## Part 2 — Model Monitor
```mermaid
flowchart LR
    A[Reference baseline] --> D[Compare]
    B[Captured production data] --> C[Scheduled monitoring job]
    C --> D
    D --> E[S3 outputs / CloudWatch metrics]
    E --> F[Alarm / investigation]
    F --> G[Review data and determine response]
```

## Part 3 — Clarify and Feature Store
```mermaid
flowchart TB
    A[Dataset and model] --> B[Clarify: facets and bias metrics]
    A --> C[Clarify: PDP / Shapley explanations]
    D[Related reusable features] --> E[Feature Group]
    E --> F[Online: fast inference retrieval]
    E --> G[Offline: historical batch data]
```

Diagrams illustrate presentation concepts only, not any live infrastructure.
