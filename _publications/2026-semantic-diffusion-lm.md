---
title: "Semantic Diffusion Language Modeling"
collection: publications
permalink: /publication/2026-semantic-diffusion-lm
excerpt: 'Investigates how the noising-kernel design in discrete diffusion language models affects training stability and generation quality. Proposes SemDLM with semantic-neighborhood diffusion, a shared refresh branch, and token-frequency prior correction. Achieves 27.19 Test PPL on LM1B.'
date: 2026-02-01
venue: 'Under review at ICML 2026'
citation: 'et al., Yuxiang Wang. "Semantic Diffusion Language Modeling." <i>Under review</i>, 2026.'
---

## Summary

A study of how the noising kernel in discrete diffusion language models affects training stability and generation quality. The work introduces a unified bias–variance trade-off framework for analyzing kernel choice.

## Method — SemDLM

- **Semantic-neighborhood diffusion** — corrupts tokens toward semantically similar tokens rather than uniformly, reducing training bias.
- **Shared refresh branch** — couples noising with a refresh mechanism that lowers training variance.
- **Token-frequency prior correction** — re-weights kernel probabilities by frequency to align training and sampling distributions.

These three choices reduce both bias and variance during training, while simultaneously strengthening the model's error-correction capacity at sampling time.

## Result

**27.19 Test PPL on LM1B**, outperforming several discrete-diffusion baselines.
