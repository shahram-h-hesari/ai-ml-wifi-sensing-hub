# Backbone Evidence Layer

The **Backbone Evidence Layer** identifies the highest-value papers, datasets, code resources, and benchmark materials supporting the **AI/ML WiFi Sensing Hub**.

This layer separates evidence into two complementary groups:

1. **Conceptual Backbone Papers** — proof-of-concept papers that justify the research problem, threat model, security gap, clinical-safety framing, or defense theory.
2. **Reproducibility Backbone Resources** — datasets, code repositories, benchmark papers, and experimental resources that support verification, reproduction, or claim checking.

This distinction is important because not every important paper needs to provide a public dataset or GitHub repository. Some papers are important because they prove that a security risk, sensing task, or defense direction is scientifically valid. Other resources are important because they provide public data, code, or benchmarks that can be inspected and reused.

---

## Why This Layer Matters

A professional evidence hub should separate two different kinds of value:

| Evidence Type | Main Question | Example Value |
|---|---|---|
| Conceptual / proof-of-concept value | Does this paper justify the research problem or technical direction? | Physical-layer attack, apnea attack/defense, CSI manipulation, certified defense theory |
| Reproducibility value | Can the dataset, code, or benchmark be inspected and reused? | Public dataset, GitHub repository, benchmark library, reproducible baseline |

This structure helps avoid treating all papers equally. The first group explains **why the research problem matters**. The second group supports **how experiments and claims can be checked**.

---

# A. Conceptual Backbone Papers

These papers justify the core research idea: **AI/ML WiFi sensing systems are useful, but CSI measurements are physically attackable, and robustness should be evaluated using safety-relevant metrics and software/certified defenses.**

These papers are included primarily for **proof-of-concept value**, not because they necessarily provide public datasets or GitHub repositories.

## Ranked Conceptual Backbone Table

| Rank | Release Year | Paper Title | Main Proof-of-Concept Role | Online Paper Link |
|---|---:|---|---|---|
| 1 | 2024 | Practical Adversarial Attack on WiFi Sensing Through Unnoticeable Communication Packet Perturbation | Shows that WiFi sensing can be attacked through communication-packet / preamble-related perturbation without breaking normal network security | [ACM DL](https://dl.acm.org/doi/10.1145/3636534.3649367) |
| 2 | 2023 | Adversarial Attack and Defense for WiFi-based Apnea Detection System | Shows healthcare-relevant WiFi sensing can be degraded by adversarial attacks and partially defended | [PDF](https://www.eng.auburn.edu/~szm0001/papers/infocom23_poster.pdf) |
| 3 | 2025 | Adversarial OFDM Spectrum Modification to Manipulate Channel State Information Systems | Shows OFDM-aware subcarrier-level manipulation of CSI measurements | [DOI](https://doi.org/10.1109/DySPAN64764.2025.11115902) |
| 4 | 2024 | Security Analysis of WiFi-based Sensing Systems: Threats from Perturbation Attacks | Shows black-box / universal perturbation threats against WiFi sensing services | [arXiv](https://arxiv.org/abs/2404.15587) |
| 5 | 2019 | Certified Adversarial Robustness via Randomized Smoothing | Provides the certified robustness theory that can motivate software-only robustness guarantees | [PMLR](https://proceedings.mlr.press/v97/cohen19c.html) / [GitHub](https://github.com/locuslab/smoothing) |

## Conceptual Backbone Comparison

The five conceptual backbone papers serve different roles in the research argument. **Practical Adversarial Attack on WiFi Sensing Through Unnoticeable Communication Packet Perturbation** is the strongest proof-of-concept for the central physical-layer threat: it shows that WiFi sensing can be attacked through packet/preamble-related perturbation while normal communication may still appear functional. This paper is the main reason the hub treats CSI as an attackable measurement rather than a trusted sensing signal.

**Adversarial Attack and Defense for WiFi-based Apnea Detection System** moves the argument from general WiFi sensing into healthcare-relevant sensing. It shows that adversarial attacks can degrade a WiFi-based apnea detection system and that defense must be evaluated directly, not assumed. This is important because apnea is closer to the kind of patient-safety application where missed or suppressed alarms matter.

**Adversarial OFDM Spectrum Modification to Manipulate Channel State Information Systems** strengthens the electrical-engineering foundation of the hub. While the first two papers show that attacks matter, this paper helps explain why the physical layer itself is a realistic attack surface by focusing on OFDM subcarrier-level manipulation of CSI. It supports the idea that attacks on WiFi sensing are not only software-level adversarial examples but can also be tied to waveform and subcarrier behavior.

**Security Analysis of WiFi-based Sensing Systems: Threats from Perturbation Attacks** broadens the threat model by emphasizing perturbation and black-box-style risks across WiFi sensing systems. It helps prevent the hub from becoming too narrow around a single attack mechanism or single model assumption. This paper supports the need to evaluate transferability, generalization, and robustness across sensing tasks.

**Certified Adversarial Robustness via Randomized Smoothing** is different from the first four papers because it is not a WiFi sensing paper. Its role is theoretical: it provides the foundation for certified robustness and software-only hardening. In this hub, it helps connect adversarial WiFi sensing to a broader trustworthy-AI framework where the goal is not only to recover average accuracy, but to reason about worst-case perturbation bounds.

Together, these conceptual papers explain **why the research problem is real**: WiFi sensing is useful, CSI can be manipulated, healthcare-relevant sensing can be harmed, the attack model can be physical-layer aware, and software/certified defenses provide a path toward safer evaluation.

---

# B. Reproducibility Backbone Resources

These resources support actual experiments, benchmark design, dataset/code verification, or claim checking.

Unlike the conceptual backbone, this section should prioritize resources with visible public code, datasets, benchmark pages, or GitHub repositories.

## Ranked Reproducibility Backbone Table

| Rank | Release Year | Paper / Resource Title | Why It Matters for Reproducibility | Public Dataset / Project Page | GitHub / Code Link |
|---|---:|---|---|---|---|
| 1 | 2023 | SenseFi: A Library and Benchmark on Deep-Learning-Empowered WiFi Human Sensing | Open-source benchmark/library for WiFi CSI human sensing using deep learning | [Paper / Dataset](https://data.mendeley.com/datasets/dzvgyxkx2f/1) | [GitHub](https://github.com/xyanchen/WiFi-CSI-Sensing-Benchmark) |
| 2 | 2025 | CSI-Bench: A Large-Scale In-the-Wild Dataset for Multi-task WiFi Sensing | Large-scale benchmark dataset for real-world WiFi sensing with multiple tasks | [Project Page](https://ai-iot-sensing.github.io/projects/project.html) / [Kaggle](https://www.kaggle.com/datasets/guozhenjennzhu/csi-bench) | [GitHub](https://github.com/Jenny-Zhu/CSI-Bench-Real-WiFi-Sensing-Benchmark/) |
| 3 | 2019 | WiAR: A Public Dataset for WiFi-Based Activity Recognition | Public WiFi activity-recognition dataset with CSI/RSSI data and example code | [Paper / Info](https://www.researchgate.net/publication/336449005_Wiar_A_Public_Dataset_for_Wifi-Based_Activity_Recognition) | [GitHub](https://github.com/linteresa/WiAR) |
| 4 | 2017 | FallDeFi: Ubiquitous Fall Detection using Commodity Wi-Fi Devices | Fall-detection resource with public GitHub repository and dataset/code links to inspect | [Paper](https://www.davidrojas.co.uk/wp-content/uploads/2017/10/falldefi_ubiquitous_fall_detection_wifi.pdf) | [GitHub](https://github.com/dmsp123/FallDeFi) |
| 5 | 2024 | MM-Fi: Multi-Modal Non-Intrusive 4D Human Dataset for Versatile Wireless Sensing | Public multimodal dataset including WiFi CSI; useful for future WiFi sensing expansion and cross-modal evaluation | [Project Page](https://ntu-aiot-lab.github.io/mm-fi) | [GitHub](https://github.com/ybhbingo/MMFi_dataset) |

## Reproducibility Backbone Comparison

The five reproducibility backbone resources serve a different purpose from the conceptual papers. They are not included only because they motivate the research problem; they are included because they provide a path for checking claims, inspecting datasets, reviewing code, or building experiments.

**SenseFi: A Library and Benchmark on Deep-Learning-Empowered WiFi Human Sensing** is the strongest starting point for reproducible AI/ML WiFi sensing because it is structured as a benchmark/library. It is valuable for comparing models, understanding common preprocessing flows, and building baseline experiments before adding adversarial testing or clinical-safety mappings.

**CSI-Bench: A Large-Scale In-the-Wild Dataset for Multi-task WiFi Sensing** is important because it addresses a weakness in many WiFi sensing studies: small, controlled, room-specific datasets. CSI-Bench is valuable for thinking about generalization across environments, users, tasks, and real-world deployment variability. For this hub, it is especially useful as a benchmark-style resource that can support broader claims about WiFi sensing beyond a single laboratory setting.

**WiAR: A Public Dataset for WiFi-Based Activity Recognition** is a practical public dataset resource for activity recognition. It may not be as broad as CSI-Bench or as library-oriented as SenseFi, but it is useful because it provides accessible WiFi sensing data that can support early baseline experiments, model testing, and potentially adversarial robustness experiments after preprocessing.

**FallDeFi: Ubiquitous Fall Detection using Commodity Wi-Fi Devices** is especially important for the healthcare-relevant direction of the hub because fall detection is one of the first target applications. Its value comes from connecting WiFi sensing to a concrete safety-related task and providing a public GitHub resource that readers can inspect. This makes it a strong candidate for fall-detection reproducibility tracking.

**MM-Fi: Multi-Modal Non-Intrusive 4D Human Dataset for Versatile Wireless Sensing** expands the hub beyond traditional CSI-only activity recognition. Because it is multimodal and includes WiFi CSI, it can support future work comparing WiFi sensing with other modalities and richer human-perception labels. It may be less directly tied to the first healthcare category than FallDeFi, but it is valuable for future expansion of the AI/ML WiFi Sensing Hub.

Together, these reproducibility resources explain **how the research can become inspectable and useful to others**: SenseFi supports benchmark code, CSI-Bench supports large-scale real-world evaluation, WiAR supports public activity-recognition data, FallDeFi supports healthcare-relevant fall-detection reproducibility, and MM-Fi supports future multimodal WiFi sensing expansion.

---

## Current Status

This folder organizes the first high-value evidence layer for the **AI/ML WiFi Sensing Hub**.

The current version starts with **5 conceptual backbone papers** and **5 reproducibility backbone resources**. The list can later expand to 10 items in each category after links, datasets, code repositories, and claims are reviewed.
