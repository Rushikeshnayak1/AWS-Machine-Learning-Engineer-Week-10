# Study Notes — Part 2: SageMaker Model Monitor

## Why monitor?
Model evaluation describes performance on historical/test data. Incoming production data and business conditions can change later. A deployed service may remain available while predictive reliability changes.

## Monitoring components
1. Establish baseline statistics on representative data.
2. Schedule monitoring analysis at an interval appropriate to risk and volume.
3. Run a monitoring job against captured production data.
4. Store detailed outputs in S3 and use CloudWatch metrics/alarms for investigation.

## Monitoring types
| Type | Main question | Evidence |
|---|---|---|
| Data quality | Have input distributions, missing values or other input properties changed? | Production feature data compared with baseline |
| Model quality | Are predictions performing as expected? | Predictions plus actual outcomes/ground truth |
| Bias drift | Are outcome patterns changing across defined groups? | Group/facet comparisons |
| Feature attribution drift | Is the model depending on features differently? | Changes in feature contributions/rankings; NDCG discussed in slides |

## Important distinctions
Input drift is not identical to lower accuracy. Model-quality measurement depends on obtaining ground-truth labels; input data monitoring may work before labels arrive. A drifting feature-importance ranking is different from bias in group outcomes.

## When an alert occurs
Confirm the signal → inspect affected data and pipeline changes → assess the cause → consider remediation or retraining only when evidence supports it. Alerts are signals for investigation, not proof that automatic retraining is necessary.

**Reference:** `Presentations/Part-2-SageMaker-Model-Monitor.pptx`.
