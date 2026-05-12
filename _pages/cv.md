---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* **M.S. in Artificial Intelligence**, *Fudan University*, 2025.09 – 2028.06 (expected)
  * School of Data Science, Knowledge Works Lab
  * Admitted via recommendation (推免)
  * Core courses: NLP & LLM, Multimodal LLMs, Frontier AI Algorithms, Optimization Theory, Deep Learning
* **B.Eng. in Computer Science (Honors Class)**, *Hangzhou Dianzi University (Zhuoyue Honor College)*, 2021.09 – 2025.06
  * GPA: **4.59 / 5.0** (Top **0.6%** of major)
  * Outstanding Graduate of HDU

Honors & Awards
======
* National Scholarship (国家奖学金)
* Provincial Government Scholarship (省政府奖学金)
* Outstanding Graduate of HDU (校优秀毕业生)
* Lead PI, National-level College Student Innovation Project (国家级大创负责人)
* CUMCM (China) — National Second Prize & Provincial First Prize
* MCM/ICM — Meritorious Winner (M Prize)
* Huawei Software Elite Challenge — Third Prize
* 10+ additional competition awards
* Member of HDU ACM Training Team

Research Experience
======
**Locality-aware Diffusion Language Modeling** &nbsp;·&nbsp; *Sole first author* &nbsp;·&nbsp; 2025.10 – 2026.03
* Systematically studied the trainability of Masked Diffusion LMs vs. autoregressive LLMs across structured generation tasks, exposing how inductive bias interacts with task dependency structure.
* Designed three controlled tasks — **in-context linear regression**, **star-graph path-finding**, and **Sudoku** — covering local exact binding, reverse planning, and global constraint satisfaction.
* Proposed two locality-aware blockwise diffusion architectures: **Scatter** ("intra-block AR + inter-block synchronous update") and **Jigsaw** ("intra-block AR + inter-block entropy-guided dynamic programming"), unifying local ordering with global iterative refinement.
* Findings: AR is better suited for local binding & sequential generation; Diffusion is better suited for global planning & constraint satisfaction. Provides empirical foundations for dLLM architecture design and future Agent planning research.

**STM: Spatio-Temporal Distance and Frame-Based Dynamic Graph Fraud Detection** &nbsp;·&nbsp; *First author (CCF-B), Invention Patent* &nbsp;·&nbsp; 2023.04 – 2024.08
* Identified that conventional GNN-based fraud detectors fail to fully exploit spatio-temporal information on dynamic graphs.
* Proposed **STM**, combining graph condensation, distance-aware intra-frame aggregation, and difference-aware inter-frame aggregation to capture both short- and long-range temporal–spatial signals.
* Achieved **SOTA** on multiple dynamic-graph fraud-detection benchmarks. Outcome: CCF-B publication and granted invention patent.

**Semantic Diffusion Language Modeling (SemDLM)** &nbsp;·&nbsp; *Co-author*
* Studied how the noising kernel design in discrete diffusion LMs affects training stability and generation quality; proposed a unified bias–variance trade-off framework.
* Proposed **SemDLM**: semantic-neighborhood diffusion + shared refresh branch + token-frequency prior correction reduces training bias/variance and strengthens sampling-time error correction.
* Result: **27.19 Test PPL on LM1B**, outperforming multiple discrete diffusion baselines.

Industry Experience
======
**Research Intern — AI4S / Multimodal LLM**, *Alibaba* &nbsp;·&nbsp; 2025.10 – Present
* Direction: protein/small-molecule unified multimodal foundation models, protein generation/understanding evaluation, and Protein Agent post-training.

* **Project I — ProtText-Eval: A Unified Evaluation Framework for Text-Guided Protein Design**
  * Solely responsible for designing and shipping the full evaluation infrastructure.
  * Built a 4-tier, 26-metric evaluation suite covering biological-plausibility filtering, instruction alignment, and task-specific capabilities.
  * Designed the modular intermediate protocol `ProteinSample → Adapter → ProteinPrediction`, decoupling models / metrics / datasets for plug-and-play extension.
  * Engineered **PDBPool** with MD5 dedup + persistent caching, dramatically improving structure-prediction throughput.
  * Integrated 5+ baseline models and ran 8+ benchmark evaluations; supports both generation and editing evaluation paradigms.

* **Project II — Protein-Function Understanding Agent (ReAct + RL)**
  * Core designer/developer of agent architecture, tool system, and the RL training pipeline.
  * Built a multi-turn `Thought → Action → Observation` rollout engine with a `Teacher Backend` abstraction supporting both local heuristics and external LLM teacher models.
  * Built a registry/execution system covering **18 bioinformatics tools**; ported 6+ core tools (mmseqs2, hmmscan, tmbed, signalp, ...) to a native backend; designed a layered dependency mechanism to remove implicit tool coupling.
  * Built end-to-end data closure on Alibaba's `ROLL` & `ROCK` frameworks: rollout → trajectory export → SFT/RL config generation → dual evaluation (ROCK tool-call metrics + ProtText biological plausibility).
  * Designed a multi-dimensional reward (answer quality, tool selection, reasoning quality, execution efficiency) for **GRPO** RL training.

* **Project III — Unified Multimodal Protein Foundation Model (Understanding + Generation)**
  * Co-designed protein-modality training strategy and the SFT / inference pipeline.
  * Built around a **MoT (Mixture-of-Transformer)** backbone supporting bidirectional `protein ↔ text` modeling.
  * Three-stage training: Stage 1 — protein pretraining on UniRef50 (~59M sequences); Stage 2 — protein–text alignment on SwissProt; Stage 3 — SFT for QA / caption / design.
  * Implemented protein/text mixed packed sequences, unified next-token loss (text CE + protein CE), and token-level MoT routing.
  * Built protein understanding & reasoning capabilities: `protein + question → answer`, sequence-likelihood scoring, and **ProteinGym** evaluation.
  * Implemented decoupled two-stage training (Stage 1 → Stage 2 checkpoint init) with large-scale distributed training support.
* **Stack**: Python, Linux, PyTorch, Transformers; Accelerate, DeepSpeed; FlashAttention-2, vLLM; Docker, SLURM, WandB; verl / ROLL, GRPO.

**Algorithm Engineer Intern — Intelligent Driving (VLA Dept.)**, *Tianyi Transportation Tech* &nbsp;·&nbsp; 2025.04 – 2025.07
* Co-designed and shipped an automated 4D pre-labeling pipeline for autonomous-driving data, integrating multiple open-source models for map/road prediction, 3D detection, semantic generation, and Occupancy prediction.
* Owned debugging, adaptation, and integration across heterogeneous open-source algorithms; resolved I/O-format / inference-flow / result-alignment incompatibilities to deliver a unified labeling chain.
* Improved pre-labeling efficiency and multi-task coordination via toolchain & automation work, providing high-quality data for large-scale AD training.
* **Stack**: PyTorch, CUDA, Linux, Docker, OpenPCDet, MMDetection3D, OpenCV.

Skills
======
* **Languages**: C++, Python, Matlab
* **ML / DL**: PyTorch, Transformers, Accelerate, DeepSpeed, FlashAttention-2, vLLM
* **RLHF**: verl, ROLL, GRPO
* **Engineering**: Docker, SLURM, WandB, Git, Linux, GPU cluster operations
* **AI Coding Tools**: Claude Code, OpenClaw — awarded department's Top Code Contributor of the Month and presented internal AI-Coding talks
* **Math foundation**: Mathematical Analysis, Linear Algebra, Operations Research — all 90+ at HDU; HDU ACM training-team member

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
