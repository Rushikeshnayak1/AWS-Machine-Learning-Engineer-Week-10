# Study Notes — Part 1: SageMaker Data Wrangler

## Why preparation matters
Input datasets can contain nulls, outliers, inconsistent formats and class imbalance. Preparation changes the statistical interpretation of the features a model receives. A repeatable flow also makes analysis more reproducible.

## Four-stage workflow
1. Import data from a supported source.
2. Preview records and investigate distributions.
3. Apply transformations and evaluate feature quality.
4. Export the flow for repeatable processing/training workflows.

## Source access
The slides mention Amazon S3/Athena, Redshift, Lake Formation and JDBC. Studio role permissions and underlying data-source authorization are distinct requirements.

## Profiling and transformation
Inspect column meaning and data types before choosing a transformation. Use visualizations to spot skew, anomalies and category imbalance. Built-in operations cover common cases; custom pandas, PySpark or PySpark SQL can support specialized rules.

## Special topics
- **Imbalance:** oversampling, undersampling and SMOTE are alternatives with different tradeoffs.
- **Missing values vs. outliers:** separate data-quality concerns requiring context-sensitive handling.
- **Images:** resizing/enhancement/controlled corruption can support preparation or resilience testing.
- **PCA:** reduces feature dimensionality, potentially reducing computational cost while making components less directly interpretable.
- **Quick Model:** early directional feedback, not production approval.

## Integration and troubleshooting
Exporting preparation flows can support managed processing/pipelines and Feature Store workflows. Check IAM, source access and Studio quotas when failures occur.

**Reference:** `Presentations/Part-1-SageMaker-Data-Wrangler.pptx`.
