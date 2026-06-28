# Scenario: UNICEF Child Malnutrition Dashboard

## Overview

An autonomous Development Intelligence Coding Assistant is building an interactive UNICEF child malnutrition dashboard using SDMX datasets.

The assistant has already completed data ingestion, cleaning, validation, and visualization.

During dashboard generation, it encounters a methodological decision that cannot be resolved from the available data or repository documentation.

Rather than making an assumption, the assistant escalates the decision to the human developer using Vocal Bridge.

---

# Objective

Demonstrate how Voice AI enables safe human oversight during autonomous data engineering workflows.

The assistant remains fully autonomous for routine tasks while requesting human judgment only when required.

---

# Workflow

```
Load UNICEF SDMX dataset
        │
        ▼
Clean and validate indicators
        │
        ▼
Generate dashboard
        │
        ▼
Decision required
        │
        ▼
Launch Vocal Bridge
        │
        ▼
Call developer
        │
        ▼
Receive spoken decision
        │
        ▼
Confirm decision
        │
        ▼
Resume dashboard generation
```

---

# Decision Required

The dashboard supports two valid aggregation strategies for international comparison.

### Option A

Use the latest available observation for each country.

Advantages

* reflects the most recent data
* easier for policymakers to interpret
* suitable for operational monitoring

---

### Option B

Use a five-year average.

Advantages

* reduces short-term fluctuations
* improves cross-country comparability
* better for long-term trend analysis

---

Both approaches are statistically valid.

The preferred methodology depends on the reporting objective and cannot be inferred automatically.

---

# Voice Escalation

The assistant pauses execution and places a Vocal Bridge call.

Example message:

> Hello. Your Development Intelligence Coding Assistant needs your decision before continuing.

> The UNICEF dashboard supports two aggregation methods.

> Option one uses the latest available observation.

> Option two uses a five-year average.

> Which approach should I use?

---

# Human Response

Developer:

> Use the latest available observation.

---

# Confirmation

Assistant:

> Decision confirmed.

> I will generate the dashboard using the latest available observation.

> Thank you.

---

# Resume Execution

The assistant immediately resumes autonomous execution.

Remaining tasks include:

* dashboard generation
* KPI calculation
* visualization rendering
* report creation
* repository updates

No further human interaction is required.

---

# Why Escalation Was Necessary

The decision was not a technical problem.

It required domain expertise and analytical judgment.

Choosing the wrong methodology could produce misleading international comparisons despite the code being technically correct.

---

# Safety Benefits

This workflow demonstrates responsible AI by ensuring that autonomous agents never guess when human expertise is required.

The assistant:

* pauses before high-impact decisions
* explains the available options
* captures the human decision by voice
* confirms the decision
* resumes execution safely

---

# Real-World Applications

The same pattern can support:

* UNICEF data analysis
* WHO health reporting
* SDG monitoring
* Climate resilience dashboards
* Humanitarian analytics
* Government statistical systems
* Research data pipelines
* AI governance workflows

---

# Key Takeaway

Voice escalation transforms human oversight from a blocking interruption into a lightweight collaboration mechanism.

Instead of waiting indefinitely or making risky assumptions, autonomous agents ask the right person at the right time and continue working once a decision has been made.