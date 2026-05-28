---

## Backbone Evidence Model

The backbone layer is organized around two complementary evidence types. The first group explains **why the research problem is scientifically important**. The second group explains **how claims can be inspected, reproduced, or tested**.

```mermaid
flowchart LR
    A["AI/ML WiFi Sensing Hub"] --> B["Conceptual Backbone"]
    A --> C["Reproducibility Backbone"]

    B --> B1["Proof of Concept"]
    B --> B2["Threat Model"]
    B --> B3["Clinical / Safety Motivation"]
    B --> B4["Defense Theory"]

    C --> C1["Public Dataset"]
    C --> C2["GitHub Repository"]
    C --> C3["Benchmark Library"]
    C --> C4["Reusable Baseline"]

    B1 --> D["Research Direction"]
    B2 --> D
    B3 --> D
    B4 --> D

    C1 --> E["Experiment Path"]
    C2 --> E
    C3 --> E
    C4 --> E

    D --> F["Stronger Research Foundation"]
    E --> F

    classDef hub fill:#0B1F3A,stroke:#0B1F3A,color:#ffffff;
    classDef concept fill:#154734,stroke:#154734,color:#ffffff;
    classDef repro fill:#1F6F5B,stroke:#1F6F5B,color:#ffffff;
    classDef output fill:#343D5E,stroke:#343D5E,color:#ffffff;

    class A hub;
    class B,B1,B2,B3,B4 concept;
    class C,C1,C2,C3,C4 repro;
    class D,E,F output;
```

---

## Backbone Review Workflow

Each candidate paper or resource is reviewed based on its main value to the hub.

```mermaid
flowchart TD
    A["Candidate Paper / Dataset / Code Resource"] --> B{"What is its main value?"}

    B --> C["Conceptual Value"]
    B --> D["Reproducibility Value"]

    C --> C1["Does it prove a key idea?"]
    C1 --> C2["Attack feasibility, clinical risk, security gap, or defense theory"]
    C2 --> C3["Add to Conceptual Backbone Table"]

    D --> D1["Can the claim be inspected?"]
    D1 --> D2["Check dataset, GitHub repo, benchmark page, code, and reuse potential"]
    D2 --> D3["Add to Reproducibility Backbone Table"]

    C3 --> E["Used for motivation and research framing"]
    D3 --> F["Used for experiments, verification, and benchmark planning"]

    E --> G["Backbone Evidence Layer"]
    F --> G

    classDef start fill:#0B1F3A,stroke:#0B1F3A,color:#ffffff;
    classDef decision fill:#D97706,stroke:#D97706,color:#ffffff;
    classDef concept fill:#154734,stroke:#154734,color:#ffffff;
    classDef repro fill:#1F6F5B,stroke:#1F6F5B,color:#ffffff;
    classDef final fill:#343D5E,stroke:#343D5E,color:#ffffff;

    class A start;
    class B decision;
    class C,C1,C2,C3,E concept;
    class D,D1,D2,D3,F repro;
    class G final;
```

---

## How to Read This Page

This page is not a simple bibliography. It separates backbone evidence into two layers:

| Layer | Reader should understand |
|---|---|
| Conceptual Backbone | These papers justify the research direction and show that the problem is real |
| Reproducibility Backbone | These resources provide datasets, GitHub repositories, benchmarks, or reusable materials that can help verify claims |

A strong research project needs both. Conceptual papers explain the scientific motivation. Reproducibility resources make the project inspectable, testable, and useful to other researchers.
