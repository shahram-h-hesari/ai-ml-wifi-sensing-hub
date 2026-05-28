---

## Review Workflow

```mermaid
flowchart TD
    A["Candidate Paper / Dataset / Code Resource"] --> B{"Main value to the hub?"}

    B -- "Proof-of-concept value" --> C["Conceptual Backbone"]
    B -- "Dataset / Code / Benchmark value" --> D["Reproducibility Backbone"]

    C --> C1["Explains why the research problem matters"]
    C1 --> C2["Threat model, attack feasibility, clinical-safety gap, or defense theory"]
    C2 --> C3["Add to Conceptual Backbone Table"]

    D --> D1["Supports inspection or reuse"]
    D1 --> D2["Check public dataset, GitHub repo, benchmark page, or reusable baseline"]
    D2 --> D3["Add to Reproducibility Backbone Table"]

    C3 --> E["Used for research motivation and thesis framing"]
    D3 --> F["Used for experiments, verification, and benchmark planning"]

    E --> G["Backbone Evidence Layer"]
    F --> G

    classDef start fill:#0B1F3A,stroke:#0B1F3A,color:#FFFFFF;
    classDef decision fill:#D97706,stroke:#92400E,color:#FFFFFF;
    classDef concept fill:#154734,stroke:#154734,color:#FFFFFF;
    classDef repro fill:#1F6F5B,stroke:#1F6F5B,color:#FFFFFF;
    classDef output fill:#343D5E,stroke:#343D5E,color:#FFFFFF;

    class A start;
    class B decision;
    class C,C1,C2,C3,E concept;
    class D,D1,D2,D3,F repro;
    class G output;
```

---

## How to Read This Workflow

The review workflow separates two kinds of backbone evidence:

| Path | Meaning |
|---|---|
| **Conceptual Backbone** | Papers that prove the research problem is real or justify the technical direction |
| **Reproducibility Backbone** | Papers, datasets, benchmarks, or GitHub repositories that help verify claims or support experiments |

The goal is to avoid mixing **proof-of-concept evidence** with **reproducible experiment resources**. Both are important, but they serve different roles in the hub.
