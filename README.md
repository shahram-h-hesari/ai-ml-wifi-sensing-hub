# AI/ML WiFi Sensing Hub

<p align="center">
  <strong>An open research hub mapping AI/ML WiFi sensing papers, datasets, code, reproducibility, and security gaps, starting with healthcare-relevant sensing.</strong>
</p>

<p align="center">
  <img alt="Focus" src="https://img.shields.io/badge/Focus-AI%2FML%20WiFi%20Sensing-154734">
  <img alt="First Category" src="https://img.shields.io/badge/First%20Category-Healthcare--Relevant%20Sensing-1F6F5B">
  <img alt="Security" src="https://img.shields.io/badge/Security-Robustness%20%26%20Privacy-0B1F3A">
  <img alt="Clinical Disclaimer" src="https://img.shields.io/badge/Clinical%20Claims-Research%20Only-8A1C1C">
</p>

---

## Overview

The **AI/ML WiFi Sensing Hub** is an open research mapping initiative focused on organizing scientific evidence around **WiFi sensing systems powered by artificial intelligence and machine learning**.

The hub maps research papers, datasets, code releases, reproducibility notes, security relevance, and open research gaps across WiFi-based sensing applications. The first focus area is **healthcare-relevant sensing**, including contactless monitoring, activity recognition, fall detection, respiration estimation, and care-aware environments.

The long-term goal is to make the AI/ML WiFi sensing research landscape easier to understand, compare, reproduce, and extend.

---

## Research Motivation

WiFi sensing has shown promise for detecting and interpreting human activity, motion, respiration, presence, and environment-level changes without requiring wearable devices or cameras. AI/ML methods are increasingly used to classify patterns, estimate signals, and support higher-level sensing applications from WiFi channel information.

However, the field still faces important challenges:

- Dataset availability and comparability
- Code availability and reproducibility
- Model robustness under noise, domain shift, and environmental change
- Security risks at the wireless and physical layers
- Privacy and spoofing concerns
- Lack of standardized evaluation across tasks and environments
- Limited connection between sensing failures and real-world application risks

This hub is designed to organize that evidence in a structured, transparent, and collaboration-friendly way.

---

## Current Focus Area: Healthcare-Relevant WiFi Sensing

The first category in this hub focuses on **healthcare-relevant and care-aware WiFi sensing**, including:

- Fall detection
- Activity recognition
- Respiration monitoring
- Vital-sign-related sensing
- Aging-in-place research
- Assisted-living environments
- Non-invasive monitoring studies
- Safety-aware sensing evaluation

This project does not claim clinical validation or medical-device readiness. The focus is research evidence mapping, reproducibility, security analysis, and trustworthy AI/ML sensing methods.

---

## Future Expansion Areas

While healthcare-relevant sensing is the first category, this hub is designed to grow into other AI/ML WiFi sensing areas, such as:

| Future Category | Example Topics |
|---|---|
| Smart Environments | Occupancy, room-level activity, behavior patterns |
| Human Activity Recognition | Gesture, movement, posture, daily activities |
| Security and Privacy | Spoofing, adversarial attacks, physical-layer risks, privacy leakage |
| Robotics and Interaction | Device-free interaction, localization, environment awareness |
| Industrial and IoT Sensing | Presence detection, monitoring, automation, anomaly detection |
| Reproducible WiFi Sensing | Public datasets, baselines, code releases, benchmark design |

---

## Project Direction

| Direction | Purpose |
|---|---|
| Scientific Evidence Mapping | Curate and classify papers, datasets, methods, and open gaps in AI/ML WiFi sensing |
| Healthcare-Relevant Sensing | Track evidence related to contactless monitoring, fall detection, respiration, and care-aware environments |
| Trustworthy AI/ML Sensing | Track robustness, reproducibility, and model-evaluation limitations across existing work |
| Wireless Security Analysis | Identify adversarial, physical-layer, spoofing, perturbation, and privacy-related risks |
| Open Collaboration | Create a structured place for researchers, labs, and practitioners to suggest related work, datasets, and code |

---

## Visual Research Scope

```mermaid
flowchart LR
    A["AI/ML WiFi Sensing Hub"] --> B["Scientific Literature"]
    A --> C["Datasets"]
    A --> D["Code & Reproducibility"]
    A --> E["Security & Robustness"]
    A --> F["Application Categories"]
    A --> G["Open Collaboration"]

    B --> B1["WiFi CSI Sensing"]
    B --> B2["AI/ML Methods"]
    B --> B3["Signal Processing"]
    B --> B4["Benchmark Papers"]

    C --> C1["Public Dataset Links"]
    C --> C2["Access Status"]
    C --> C3["License Notes"]
    C --> C4["Experiment Suitability"]

    D --> D1["GitHub Repositories"]
    D --> D2["Reproducibility Notes"]
    D --> D3["Missing / Broken Code"]
    D --> D4["Baseline Methods"]

    E --> E1["Adversarial ML"]
    E --> E2["Physical-Layer Attacks"]
    E --> E3["CSI Perturbation"]
    E --> E4["Robustness Evaluation"]
    E --> E5["Privacy and Spoofing Risks"]

    F --> F1["Healthcare-Relevant Sensing"]
    F --> F2["Smart Environments"]
    F --> F3["Human Activity Recognition"]
    F --> F4["Future Categories"]

    G --> G1["Authors"]
    G --> G2["Labs"]
    G --> G3["Dataset Owners"]
    G --> G4["AI/ML WiFi Sensing Researchers"]
```

---

## Evidence Workflow

```mermaid
flowchart TD
    A["New Paper, Dataset, or Code Repository"] --> B["Evidence Intake"]
    B --> C{"Relevant to AI/ML WiFi Sensing?"}

    C -- "No" --> Z["Archived / Out of Scope"]
    C -- "Yes" --> D["Scientific Summary"]

    D --> E["Dataset & Code Availability Check"]
    E --> F["Security and Robustness Mapping"]
    F --> G["Application Category Mapping"]
    G --> H["Added to Evidence Hub"]

    H --> I{"Potential for Collaboration?"}
    I -- "Yes" --> J["Research / Lab / Community Outreach Candidate"]
    I -- "No" --> K["Internal Evidence Reference"]
```

---

## Evidence Categories

| Category | Purpose |
|---|---|
| Core Research Evidence | Papers that strongly shape the technical direction of AI/ML WiFi sensing |
| Healthcare-Relevant WiFi Sensing | Work on contactless sensing for activity, fall detection, respiration, vital signs, and care-aware environments |
| Security and Robustness Evidence | Papers on adversarial attacks, defenses, spoofing, perturbation, privacy, and physical-layer risks |
| Dataset Evidence | Public datasets, access status, licensing, modalities, endpoints, and suitability for experiments |
| Code and Reproducibility Evidence | Available repositories, reproducibility notes, baseline implementations, and missing-code gaps |
| Future Application Categories | Research connected to smart environments, human activity recognition, IoT sensing, robotics, and other WiFi sensing areas |
| Collaboration Leads | Authors, labs, datasets, and groups whose work may connect to this hub |

---

## Intended Audience

This project is designed for researchers and practitioners working across:

- AI/ML for WiFi sensing
- WiFi CSI and wireless sensing
- Healthcare-relevant sensing
- Cybersecurity and adversarial machine learning
- Reproducible research
- Aging technology and assisted-living research
- Contactless monitoring systems
- Smart environments and IoT sensing
- Trustworthy AI for sensing applications

---

## Collaboration Invitation

Suggestions are welcome for:

- Relevant papers
- Public datasets
- Code repositories
- Reproducibility notes
- Missing but important related work
- Security or robustness gaps
- Research groups or labs working in related areas
- New application categories for AI/ML WiFi sensing

Future GitHub issue templates will provide a structured way to suggest papers, datasets, code resources, and collaboration ideas.

---

## Research Disclaimer

This project is a research evidence hub. It does **not** claim clinical validation, medical-device readiness, real patient deployment, regulatory approval, or diagnostic capability.

The focus is scientific evidence mapping, reproducibility, security analysis, and trustworthy AI/ML sensing methods for WiFi-based sensing applications.

---

## Current Status

This hub is under active development as a structured research resource for AI/ML WiFi sensing, starting with healthcare-relevant and care-aware sensing applications.
