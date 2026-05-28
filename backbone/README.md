# Backbone Evidence Layer

The **Backbone Evidence Layer** identifies the highest-value papers, datasets, code resources, and benchmark materials supporting the **AI/ML WiFi Sensing Hub**.

This layer separates evidence into three complementary groups currently tracked in this folder:

1. **Conceptual Backbone Papers** — proof-of-concept papers that justify the research problem, threat model, security gap, safety framing, or defense theory.
2. **Reproducibility Backbone Resources** — datasets, code repositories, benchmark papers, and experimental resources that support verification, reproduction, or claim checking.
3. **Adversarial Impact Backbone** — papers showing that adversarial, perturbation, spoofing, physical-layer, black-box, or transfer attacks degrade WiFi CSI sensing or closely related wireless sensing outputs.

A separate **Clinical-Safety Translation Backbone** can be added later for HR, RR, fall safety, false alarms, missed events, and time-to-alarm references.

---

## Why This Layer Matters

A professional evidence hub should separate different kinds of value:

| Evidence Type | Main Question | Example Value |
|---|---|---|
| Conceptual / proof-of-concept value | Does this paper justify the research problem or technical direction? | Physical-layer attack, CSI manipulation, adversarial sensing risk, certified defense theory |
| Reproducibility value | Can the dataset, code, or benchmark be inspected and reused? | Public dataset, GitHub repository, benchmark library, reproducible baseline |
| Adversarial-impact value | Does the paper show measurable sensing degradation under attack? | Attack success rate, accuracy drop, regression error, false prediction rate, targeted misclassification |

This structure helps avoid treating all papers equally. Some papers explain **why the research problem matters**. Some provide **datasets or code for experiments**. Others provide **attack-impact evidence** that can be translated into HR, RR, and fall-related clinical-safety metrics.

---

# A. Conceptual Backbone Papers

These papers justify the core research idea: **AI/ML WiFi sensing systems are useful, but CSI measurements are physically attackable, and robustness should be evaluated using safety-relevant metrics and software/certified defenses.**

These papers are included primarily for **proof-of-concept value**, not because they necessarily provide public datasets or GitHub repositories.

## Ranked Conceptual Backbone Table

| Rank | Release Year | Paper Title | Main Proof-of-Concept Role | Online Paper Link |
|---|---:|---|---|---|
| 1 | 2024 | Practical Adversarial Attack on WiFi Sensing Through Unnoticeable Communication Packet Perturbation | Shows that WiFi sensing can be attacked through communication-packet / preamble-related perturbation without breaking normal network security | [ACM DL](https://dl.acm.org/doi/10.1145/3636534.3649367) |
| 2 | 2024 | Security Analysis of WiFi-based Sensing Systems: Threats from Perturbation Attacks | Shows black-box / universal perturbation threats against WiFi sensing services | [arXiv](https://arxiv.org/abs/2404.15587) |
| 3 | 2025 | Adversarial OFDM Spectrum Modification to Manipulate Channel State Information Systems | Shows OFDM-aware subcarrier-level manipulation of CSI measurements | [IEEE Xplore](https://ieeexplore.ieee.org/document/11115902/) |
| 4 | 2022 | WiCAM: Imperceptible Adversarial Attack on Deep Learning based WiFi Sensing | Shows attention-guided, subcarrier-level adversarial perturbation against WiFi sensing models | [IEEE Xplore](https://ieeexplore.ieee.org/document/9918564/) |
| 5 | 2019 | Certified Adversarial Robustness via Randomized Smoothing | Provides certified robustness theory that can motivate software-only robustness guarantees | [PMLR](https://proceedings.mlr.press/v97/cohen19c.html) / [GitHub](https://github.com/locuslab/smoothing) |

## Conceptual Backbone Comparison

The five conceptual backbone papers serve different roles in the research argument. **Practical Adversarial Attack on WiFi Sensing Through Unnoticeable Communication Packet Perturbation** [1] is the strongest proof-of-concept for the central physical-layer threat: it shows that WiFi sensing can be attacked through packet/preamble-related perturbation while normal communication may still appear functional. This paper is the main reason the hub treats CSI as an attackable measurement rather than a trusted sensing signal.

**Security Analysis of WiFi-based Sensing Systems: Threats from Perturbation Attacks** [2] broadens the threat model by emphasizing universal, black-box, and over-the-air perturbation risks across multiple WiFi sensing applications. It helps prevent the hub from becoming too narrow around a single model, dataset, or attack assumption.

**Adversarial OFDM Spectrum Modification to Manipulate Channel State Information Systems** [3] strengthens the electrical-engineering foundation of the hub. While [1] and [2] show that attacks matter, [3] helps explain why the physical layer itself is a realistic attack surface by focusing on OFDM subcarrier-level manipulation of CSI.

**WiCAM: Imperceptible Adversarial Attack on Deep Learning based WiFi Sensing** [4] supports the idea that CSI perturbations can be made selective, imperceptible, and model-aware. This is important for HR, RR, and fall-sensing systems because these systems often depend on a subset of sensitive subcarriers, antennas, or temporal patterns.

**Certified Adversarial Robustness via Randomized Smoothing** [5] is different from the first four papers because it is not a WiFi sensing paper. Its role is theoretical: it provides the foundation for certified robustness and software-only hardening. In this hub, it helps connect adversarial WiFi sensing to a broader trustworthy-AI framework where the goal is not only to recover average accuracy, but to reason about worst-case perturbation bounds.

Together, [1]–[5] explain **why the research problem is real**: WiFi sensing is useful, CSI can be manipulated, the attack model can be physical-layer aware, imperceptible adversarial perturbations are possible, and software/certified defenses provide a path toward safer evaluation.

---

# B. Reproducibility Backbone Resources

These resources support actual experiments, benchmark design, dataset/code verification, or claim checking.

Unlike the conceptual backbone, this section prioritizes resources with visible public code, datasets, benchmark pages, or GitHub repositories.

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

**SenseFi: A Library and Benchmark on Deep-Learning-Empowered WiFi Human Sensing** [1] is the strongest starting point for reproducible AI/ML WiFi sensing because it is structured as a benchmark/library. It is valuable for comparing models, understanding common preprocessing flows, and building baseline experiments before adding adversarial testing or clinical-safety mappings.

**CSI-Bench: A Large-Scale In-the-Wild Dataset for Multi-task WiFi Sensing** [2] is important because it addresses a weakness in many WiFi sensing studies: small, controlled, room-specific datasets. CSI-Bench is valuable for thinking about generalization across environments, users, tasks, and real-world deployment variability.

**WiAR: A Public Dataset for WiFi-Based Activity Recognition** [3] is a practical public dataset resource for activity recognition. It may not be as broad as CSI-Bench [2] or as library-oriented as SenseFi [1], but it is useful because it provides accessible WiFi sensing data that can support early baseline experiments, model testing, and potentially adversarial robustness experiments after preprocessing.

**FallDeFi: Ubiquitous Fall Detection using Commodity Wi-Fi Devices** [4] is especially important for the healthcare-relevant direction of the hub because fall detection is one of the first target applications. Its value comes from connecting WiFi sensing to a concrete safety-related task and providing a public GitHub resource that readers can inspect.

**MM-Fi: Multi-Modal Non-Intrusive 4D Human Dataset for Versatile Wireless Sensing** [5] expands the hub beyond traditional CSI-only activity recognition. Because it is multimodal and includes WiFi CSI, it can support future work comparing WiFi sensing with other modalities and richer human-perception labels.

Together, [1]–[5] explain **how the research can become inspectable and useful to others**: SenseFi [1] supports benchmark code, CSI-Bench [2] supports large-scale real-world evaluation, WiAR [3] supports public activity-recognition data, FallDeFi [4] supports healthcare-relevant fall-detection reproducibility, and MM-Fi [5] supports future multimodal WiFi sensing expansion.

---

# D. Adversarial Impact Backbone

The **Adversarial Impact Backbone** identifies papers showing measurable degradation of WiFi CSI sensing or closely related wireless sensing systems under attack.

This category is different from the conceptual backbone. The conceptual backbone explains **why the problem exists**. The adversarial-impact backbone explains **how attacks change model outputs** and how those changes can later be translated into HR, RR, and fall-related clinical-safety metrics.

The current evidence audit shows a clear research gap: prior work reports technical degradation such as attack success rate, accuracy drop, or misclassification rate, but it generally does **not** convert these results into clinical-safety units such as missed falls per day, HR/RR threshold violation rate, false alarms per hour, or time-to-alarm delay.

## Primary Adversarial Impact Backbone Papers

| Rank | Year | Paper Title | Main Adversarial Impact Role | Target Task | Attack Type | Link |
|---|---:|---|---|---|---|---|
| 1 | 2024 | Practical Adversarial Attack on WiFi Sensing Through Unnoticeable Communication Packet Perturbation | Practical physical-layer attack through communication-packet / preamble-related perturbation | Activity recognition, user authentication, vital-sign monitoring context | Physical-layer preamble / pilot-symbol perturbation, C&W-based optimization, universal attack | [ACM DL](https://dl.acm.org/doi/10.1145/3636534.3649367) |
| 2 | 2024 | Security Analysis of WiFi-based Sensing Systems: Threats from Perturbation Attacks | Unified black-box perturbation threat across multiple WiFi sensing applications | Gesture recognition, respiratory monitoring, user authentication, localization | Black-box universal perturbation, over-the-air attack, surrogate modeling | [arXiv](https://arxiv.org/abs/2404.15587) |
| 3 | 2022 | SecureSense: Defending Adversarial Attack for Secure Device-Free Human Activity Recognition | Closest existing paper to adversarial fall-class degradation in WiFi HAR | Human activity recognition including falling-down class | FGSM, Gaussian noise, bimodal attack, defense evaluation | [DOI](https://doi.org/10.1109/tmc.2022.3226742) |
| 4 | 2025 | Towards Trustworthy Wi-Fi Sensing: Systematic Evaluation of Deep Learning Model Robustness to Adversarial Attacks | Reproducible adversarial robustness benchmark across public CSI datasets | Activity recognition, fall-class HAR, gait identification | PGD, DeepFool, UAP, transfer, physically constrained perturbations | [arXiv](https://arxiv.org/abs/2511.20456) |
| 5 | 2023 | Adversarial Attack and Defense for WiFi-based Apnea Detection System | Closest respiratory-safety proxy paper; directly attacks breathing-derived WiFi CSI output | Apnea / respiration-related WiFi CSI classification | FGSM, PGD, C&W, adversarial training | [IEEE Xplore](https://ieeexplore.ieee.org/document/10225824/) |
| 6 | 2022 | IS-WARS: Intelligent and Stealthy Adversarial Attack to Wi-Fi-Based Human Activity Recognition Systems | Shows stealthy cross-technology physical interference against WiFi HAR | Human activity recognition, user authentication | ZigBee / Bluetooth / LTE-U cross-technology signal injection | [IEEE Xplore](https://ieeexplore.ieee.org/document/9531421/) |
| 7 | 2024 | Time to Think the Security of WiFi-Based Behavior Recognition Systems | Demonstrates physical-world attacks against behavior recognition systems with healthcare-relevant framing | WiFi behavior recognition, user authentication | Online jamming-based physical adversarial samples, targeted and untargeted attacks | [IEEE Xplore](https://ieeexplore.ieee.org/document/10080971/) |
| 8 | 2025 | Wi-Spoof: Generating Adversarial Wireless Signals to Deceive Wi-Fi Sensing Systems | Commodity-hardware spoofing attack with high targeted misclassification rate | Human activity recognition | Transmission-power manipulation, pseudo-PWM spoofing | [Elsevier](https://linkinghub.elsevier.com/retrieve/pii/S2214212625000894) |
| 9 | 2025 | Adversarial OFDM Spectrum Modification to Manipulate Channel State Information Systems | Demonstrates subcarrier-level OFDM interference that manipulates CSI itself | CSI-based authentication, localization, intrusion detection; general CSI sensing risk | OFDM subcarrier-level interference, random and targeted CSI alteration | [IEEE Xplore](https://ieeexplore.ieee.org/document/11115902/) |
| 10 | 2022 | WiCAM: Imperceptible Adversarial Attack on Deep Learning based WiFi Sensing | Introduces imperceptible, attention-guided subcarrier perturbation against WiFi sensing models | HAR, gesture recognition, user identification | Attention-mask-guided FGSM / PGD on CSI subcarriers | [IEEE Xplore](https://ieeexplore.ieee.org/document/9918564/) |

## Adversarial Impact Comparison

The ten adversarial-impact papers provide the technical bridge between WiFi CSI attack feasibility and the thesis’s clinical-safety translation framework.

**Practical Adversarial Attack on WiFi Sensing Through Unnoticeable Communication Packet Perturbation** [1] is the strongest physical-layer attack anchor because it targets the WiFi sensing pipeline near the CSI-estimation stage. Its value for the thesis is that it supports the assumption that sensing input can be corrupted while communication still appears normal.

**Security Analysis of WiFi-based Sensing Systems: Threats from Perturbation Attacks** [2] is the strongest black-box / universal-attack anchor because it evaluates attacks across multiple WiFi sensing applications, including respiratory monitoring. This makes it especially valuable for RR-related threat modeling, even though it does not directly translate respiratory degradation into clinical units.

**SecureSense: Defending Adversarial Attack for Secure Device-Free Human Activity Recognition** [3] is one of the most important fall-related papers because the WiFi HAR setting includes a falling-down class. This makes it a useful proxy for fall-detection vulnerability, even though it is still framed as activity recognition rather than clinical fall monitoring.

**Towards Trustworthy Wi-Fi Sensing** [4] is valuable because it provides a systematic adversarial robustness benchmark on public CSI datasets and includes fall-class activity recognition. It is especially important for reproducibility because it connects adversarial evaluation with public datasets and model comparisons.

**Adversarial Attack and Defense for WiFi-based Apnea Detection System** [5] should be treated as a respiratory-rate proxy, not as a main apnea-focused thesis endpoint. It is still useful because it is the closest available example of an adversarial attack on a breathing-derived WiFi CSI output.

**IS-WARS** [6] and **Time to Think the Security of WiFi-Based Behavior Recognition Systems** [7] both strengthen the physical-realism argument. They show that WiFi behavior recognition systems can be attacked in real wireless environments through stealthy or jamming-based mechanisms, which matters for elderly-home settings where multiple wireless and IoT devices may coexist.

**Wi-Spoof** [8] is important because it emphasizes accessibility of the attacker model: the attack is based on commodity hardware rather than specialized SDR-only assumptions. This is useful for framing real-world risk.

**Adversarial OFDM Spectrum Modification to Manipulate Channel State Information Systems** [9] provides the strongest OFDM/subcarrier-level CSI manipulation mechanism. Its importance is broader than one sensing task: HR, RR, and fall detection all depend on CSI integrity.

**WiCAM** [10] is important because it introduces a selective and imperceptible adversarial perturbation model for WiFi sensing. This is especially relevant to HR/RR sensing because physiological information may be concentrated in specific subcarriers, antennas, or temporal patterns.

Together, [1]–[10] show that adversarial impact on WiFi sensing is not limited to one attack style. The literature includes physical-layer preamble manipulation, black-box universal perturbations, FGSM/PGD-style CSI attacks, cross-technology signal injection, jamming-based physical attacks, commodity-hardware spoofing, OFDM subcarrier manipulation, and imperceptible subcarrier perturbations. The thesis contribution is to translate these attack effects into HR, RR, and fall-related safety metrics.

## Clinical-Safety Translation Potential

| Rank | Paper | Technical Degradation | Translation to HR/RR/Fall Metric | Confidence |
|---|---|---|---|---|
| 1 | Li et al. 2024 | High attack success against WiFi sensing tasks through packet/preamble-related perturbation | Fall false negative, fall false positive, or general sensing-input corruption; possible HR/RR corruption if applied to vital-sign models | High for fall/activity; Medium for HR/RR |
| 2 | Cao et al. 2024 / WiIntruder | Large average accuracy decrease across multiple WiFi sensing applications, including respiratory monitoring | RR estimation error, respiratory-state misclassification, false alert, or suppressed alert | High for RR proxy; Medium for fall |
| 3 | Yang et al. 2022 / SecureSense | HAR accuracy collapse under adversarial attack; includes falling-down activity class | Missed fall, false fall alarm, fall-class sensitivity loss | High for fall |
| 4 | Gopalakrishnan and Hailes 2025 | Robustness evaluation across public CSI datasets; fall-class HAR included | Fall false negative / false positive under attack; reproducible robustness baseline | High for fall; Medium for HR/RR extension |
| 5 | Ambalkar et al. 2023 | Adversarial attacks significantly degrade WiFi-based breathing/apnea classification | RR-related missed breathing event or false respiratory alert; use only as respiratory proxy | Medium to High for RR proxy |
| 6 | IS-WARS 2022 | Stealthy cross-technology interference compromises WiFi HAR systems | Fall false negative or false positive under realistic IoT coexistence interference | Medium for fall |
| 7 | Liu et al. 2024 | Physical-world targeted and untargeted attacks against behavior recognition systems | Targeted misclassification of fall vs. non-fall behavior; false safety state | High for fall proxy |
| 8 | Wi-Spoof 2025 | Targeted misclassification using commodity wireless signal manipulation | Fall false alarm or missed fall if applied to fall/non-fall classifier | High for fall proxy |
| 9 | Huang et al. 2025 / OFDM CSI Manipulation | Subcarrier-level CSI alteration at the OFDM layer | General CSI integrity failure affecting HR, RR, and fall models | Medium for all |
| 10 | WiCAM 2022 | Imperceptible attention-guided CSI perturbation degrades WiFi sensing models | Fall/activity misclassification; possible HR/RR error if applied to physiological CSI models | Medium to High |

## Supporting / Secondary Adversarial Evidence

| Candidate Rank | Year | Paper Title | Why It Is Supporting Evidence | Link |
|---|---:|---|---|---|
| 11 | 2024 | WiCAM2.0: Imperceptible and Targeted Attack on Deep Learning based WiFi Sensing | Extends WiCAM with stronger targeted attack framing; useful as follow-up evidence | [ACM DL](https://dl.acm.org/doi/10.1145/3698592) |
| 12 | 2023 | Over-the-Air Adversarial Attacks on Deep Learning Wi-Fi Fingerprinting | Strong OTA WiFi fingerprinting attack evidence, but localization/fingerprinting is less directly tied to HR/RR/fall | [IEEE Xplore](https://ieeexplore.ieee.org/document/10015738/) |
| 13 | 2022 | IRShield: A Countermeasure Against Adversarial Physical-Layer Wireless Sensing | Important physical-layer defense/countermeasure paper, but not directly an HR/RR/fall sensing attack paper | [DOI](https://doi.org/10.1109/sp46214.2022.9833676) |
| 14 | 2023 | Attack Evaluations of Deep Learning Empowered WiFi Sensing in IoT Systems | Useful multi-dataset attack evaluation context; supports broader evidence map | [IEEE Xplore](https://ieeexplore.ieee.org/document/10226121/) |
| 15 | 2025 | A Survey on Secure WiFi Sensing Technology: Attacks and Defenses | Useful taxonomy and literature map; not primary experimental backbone | [MDPI Sensors](https://www.mdpi.com/1424-8220/25/6/1913) |

## Adversarial Impact Gap Statement

The adversarial WiFi sensing literature is strong enough to justify the thesis threat model, but it is still incomplete for HR, RR, and fall-safety evaluation.

The current literature provides:

- direct physical-layer and preamble/pilot perturbation evidence,
- black-box and universal perturbation evidence,
- WiFi HAR and fall-class proxy evidence,
- respiratory-monitoring and apnea-related proxy evidence,
- OFDM subcarrier-level CSI manipulation evidence,
- physical-world attack evidence using interference, jamming, and spoofing.

However, the current literature generally does **not** provide:

- direct adversarial HR estimation studies using WiFi CSI,
- direct adversarial RR regression studies using WiFi CSI,
- direct adversarial fall-detection studies translated into missed falls per day,
- clinical false-alarm or time-to-alarm translation under attack,
- certified robustness bounds linked to HR/RR/fall safety metrics.

This gap is the research opportunity: the thesis can use the adversarial-impact papers as the attack-evidence layer, then translate technical degradation into clinically meaningful HR, RR, and fall-safety endpoints.

---

## Current Status

This folder organizes the first high-value evidence layer for the **AI/ML WiFi Sensing Hub**.

The current version contains:

- **5 Conceptual Backbone papers**
- **5 Reproducibility Backbone resources**
- **10 Primary Adversarial Impact Backbone papers**
- **5 Supporting / Secondary Adversarial Evidence papers**

Next planned addition:

- **Clinical-Safety Translation Backbone** for HR, RR, fall safety, false alarms, missed events, and time-to-alarm evidence.
