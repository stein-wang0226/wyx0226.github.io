---
title: "Semantic DLM+: Improving Diffusion Language Models through Bias-variance Trade-off in Transition Kernel Design"
collection: publications
permalink: /publication/2026-semantic-dlm-plus
excerpt: 'Analyzes how transition-kernel choices affect diffusion language models via asymptotic bias, exposure bias, and optimization variance. Revives semantic DLM and proposes SemDLM+ with a global transition kernel plus a semantic-frequency penalty to fix the semantic-basin diversity problem. Shows better training dynamics and stronger generation diversity on LM1B and OpenWebText.'
date: 2026-06-13
venue: 'arXiv preprint, 2026'
paperurl: 'https://arxiv.org/abs/2606.15327'
citation: 'Keyue Jiang, Yuxiang Wang, Yanan Zhao, Xiang Yu, Qifang Zhao, Bohan Tang, Baojian Zhou, Yanghua Xiao, Lin Qu, Xiaoxiao Xu. "Semantic DLM+: Improving Diffusion Language Models through Bias-variance Trade-off in Transition Kernel Design." <i>arXiv:2606.15327</i>, 2026.'
---

## Summary

This paper studies how the choice of transition kernel in discrete diffusion language models shapes the bias–variance trade-off across training and sampling. It connects kernel design to three key phenomena:

- **Asymptotic bias** — how the stationary distribution of the forward process biases the learned model;
- **Exposure bias** — the mismatch between training-time corruption and sampling-time model-generated prefixes;
- **Optimization variance** — the variance introduced when fitting the denoising network on finite data.

## Method — SemDLM+

Building on the semantic DLM framework, SemDLM+ introduces two key upgrades:

- **Global transition kernel** — augments the local semantic-neighborhood corruption with a globally structured transition, balancing local refinement and long-range coherence;
- **Semantic-frequency penalty** — corrects the "semantic basin" effect where the model collapses to a small set of high-frequency semantic neighbors, improving output diversity.

## Key findings

- SemDLM+ achieves better training dynamics compared to standard masked-diffusion baselines;
- Generation quality remains competitive while **diversity is improved**, addressing a known weakness of semantic-diffusion kernels;
- Evaluated on **LM1B** and **OpenWebText**.
