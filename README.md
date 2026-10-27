# AWS Machine Learning Engineer – Associate | Week 10

**Student:** Rushikesh Nayak  
**University:** Concordia University Chicago  
**Professor:** Dr. Victor Govindaswamy  
**Learning series:** AWS Certified Machine Learning Engineer – Associate  
**Week:** 10 | **Presentations:** 3

## Overview

This repository documents my Week 10 learning through three presentation-based studies of Amazon SageMaker capabilities. The goal is to understand how machine learning data is prepared, how models are monitored after deployment, and how fairness, explainability, and feature consistency fit into the ML lifecycle.

> **Scope of evidence:** The three PowerPoint presentations are the source material for this repository. The notes and diagrams summarize the concepts discussed; they do **not** claim that an AWS account, SageMaker job, live deployment, or hands-on experiment was run. Add genuine lab artifacts and screenshots if completed.

## Week 10 video series

| Part | Focus | Presentation | YouTube explanation | LinkedIn learning post |
|---|---|---|---|---|
| 1 | SageMaker Data Wrangler | [View PPT](Presentations/Part-1-SageMaker-Data-Wrangler.pptx) |[https://youtu.be/m2XsgSLpofU?si=wkVctlxEK01HzMAm] | [https://lnkd.in/p/gVg9bEZt] |
| 2 | SageMaker Model Monitor | [View PPT](Presentations/Part-2-SageMaker-Model-Monitor.pptx) | [https://youtu.be/7wWaZDTVaHU?si=5pZpxyupcseUd6AC] | [https://lnkd.in/p/gXn-kxCZ] |
| 3 | SageMaker Clarify and Feature Store | [View PPT](Presentations/Part-3-SageMaker-Clarify-and-Feature-Store.pptx) | [https://youtu.be/p3Z51uphsC4?si=L0NPdUrYR6o4CRlx] | [https://youtu.be/p3Z51uphsC4?si=L0NPdUrYR6o4CRlx] |

**Important:** Replace the six generic platform links above with your actual published video/post URLs before submitting. Links are also collected in [Links.md](Links.md).

## Learning objectives and technologies

- **Data Wrangler:** data import, profiling, built-in and custom transformation, class imbalance, image preparation, PCA, Quick Model, exporting preparation flows.
- **Model Monitor:** baselines, monitoring schedules, data quality vs. model quality, bias drift, attribution drift, Amazon S3 results, CloudWatch metrics and alarms.
- **Clarify:** fairness questions, facet-based bias analysis, statistical distance metrics, partial dependence plots, SHAP/Shapley values, temporal attribution concepts.
- **Feature Store:** Feature Groups, Record IDs, Event Time, online low-latency access, offline historical/batch access.

**Related technologies mentioned in the slides:** Amazon S3, Athena, Redshift, AWS Lake Formation, JDBC, pandas, PySpark, PySpark SQL, CloudWatch, SageMaker Processing and Pipelines.

## How the concepts connect

1. Prepare and validate data with **Data Wrangler**.
2. Train/deploy a model using the prepared features (broader lifecycle context, not a Week 10 hands-on implementation).
3. Investigate bias and explain model behavior using **Clarify** concepts.
4. Organize consistent training/inference features using **Feature Store**.
5. Observe production changes using **Model Monitor** and investigate drift alerts.

See [Diagrams/ML-Lifecycle.md](Diagrams/ML-Lifecycle.md) and [Diagrams/Week-10-Workflows.md](Diagrams/Week-10-Workflows.md).

## Repository contents

- `Presentations/`: three original Week 10 PowerPoint presentations (10 slides each).
- `Study-Notes/`: topic-by-topic notes aligned with each presentation.
- `Diagrams/`: conceptual Mermaid workflow diagrams; not screenshots of deployed AWS resources.
- `Documentation/`: progress, presentation summary, challenges and solutions, reflection, and references.
- `Lab-Notes/`: documentation template for *actual* hands-on work if performed.
- `Screenshots/`: instructions for supplying genuine video/lab/publishing evidence.
- `Code-and-Commands/`: usage note (no unverified executed commands included).
- `Links.md`: links to all public YouTube and LinkedIn posts.
- `SUBMISSION-CHECKLIST.md`: final review before GitHub/academic submission.

## Challenges and takeaways

I found it useful to separate concepts that sound similar but answer different questions: data drift versus prediction quality, fairness drift versus feature-attribution drift, and online versus offline feature access. Mapping each topic to its *specific purpose* helped make the presentations easier to understand. Read [Documentation/Challenges-and-Solutions.md](Documentation/Challenges-and-Solutions.md) for details.

## Learning approach

The work shared here consists of student-created explanations and learning notes from the three Week 10 presentations. The folder structure leaves space for genuine practical proof, such as screenshots, code, configuration, lab notes, or results, if those materials are produced later. No such evidence has been fabricated.

## Acknowledgment

Thank you to **Professor Dr. Victor Govindaswamy** for encouraging independent investigation and clear technical communication through these weekly learning activities.

## References

The three PowerPoint presentations in `Presentations/` are the primary references for this repository. See [Documentation/References.md](Documentation/References.md) for details and official AWS documentation starting points to consult for further study.
