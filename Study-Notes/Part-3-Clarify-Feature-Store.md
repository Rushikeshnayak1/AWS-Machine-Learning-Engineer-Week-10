# Study Notes — Part 3: SageMaker Clarify and Feature Store

## Responsible AI questions
- **Fairness:** who is affected by the predictions?
- **Explainability:** why was this prediction produced?

Accuracy alone does not answer either question.

## Facets and metrics
A facet defines the group being compared. Select one that fits the fairness question and domain context. The slides cover class imbalance, Difference in Positive Proportions in Labels (DPL), KL divergence, Jensen–Shannon divergence, Lp-norm, Total Variation Distance and Kolmogorov–Smirnov. Different statistics capture different aspects of distributions; none alone proves or disproves fairness.

## Model explanations
- **Partial Dependence Plots (PDP):** show estimated average model response as selected features vary. Interpret carefully when correlated features produce unrealistic combinations.
- **Shapley/SHAP:** attribute contributions to individual features using a game-theoretic perspective; approximation helps with computational complexity.
- **Asymmetric Shapley Values:** account for temporal ordering assumptions in time-series explanations.

## Feature Store
A Feature Group bundles related reusable features. Record identifiers identify entities; event time marks when the feature values apply.

| Online Store | Offline Store |
|---|---|
| Low-latency access | Historical/batch access |
| Real-time inference | Training and analytics |
| `PutRecord`, `GetRecord` highlighted on slides | S3, Athena and Data Wrangler highlighted on slides |

Shared feature definitions can reduce training-serving inconsistencies.

**Reference:** `Presentations/Part-3-SageMaker-Clarify-and-Feature-Store.pptx`.
