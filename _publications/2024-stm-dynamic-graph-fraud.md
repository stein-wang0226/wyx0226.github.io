---
title: "STM: Spatio-Temporal Distance and Frame-Based Dynamic Graph Fraud Detection"
collection: publications
permalink: /publication/2024-stm-dynamic-graph-fraud
excerpt: 'Proposes STM, a dynamic-graph fraud-detection model that combines graph condensation, distance-aware intra-frame aggregation, and difference-aware inter-frame aggregation to fully exploit short- and long-range spatio-temporal information. Achieves SOTA on multiple dynamic-graph benchmarks. Also resulted in an invention patent.'
date: 2024-08-01
venue: 'CCF-B venue'
citation: 'Yuxiang Wang, et al. "Spatio-Temporal Distance and Frame-Based Dynamic Graph Fraud Detection." 2024.'
---

## Motivation

Conventional GNN-based fraud detectors struggle to fully exploit the rich spatio-temporal structure present in dynamic graphs, leaving long-range temporal signals and inter-frame discrepancies underused.

## Method — STM

STM decomposes the dynamic graph into frames and applies multiple complementary modules:

- **Graph condensation** — compresses the per-frame substructure into compact, learnable summaries.
- **Distance-aware intra-frame aggregation** — aggregates neighborhood signals weighted by spatio-temporal distance.
- **Difference-aware inter-frame aggregation** — captures behavioral drift across frames to surface emerging fraud patterns.

Together these modules let STM exploit both short-term and long-term temporal information alongside spatial structure, improving both detection accuracy and efficiency.

## Outcomes

- **SOTA** on multiple dynamic-graph fraud-detection benchmarks
- Granted **invention patent**
- Funded as a **National-level College Student Innovation Project** (lead PI)
