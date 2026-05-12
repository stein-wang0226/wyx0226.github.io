---
title: "Locality-aware Diffusion Language Modeling"
collection: publications
permalink: /publication/2026-locality-aware-dlm
excerpt: 'Studies the trainability of Masked Diffusion Language Models against autoregressive LLMs across structured generation tasks. Proposes two locality-aware blockwise diffusion architectures (Scatter and Jigsaw) bridging AR-style local ordering and Diffusion-style global iterative refinement.'
date: 2026-03-01
venue: 'arXiv preprint, 2026'
paperurl: 'https://arxiv.org/abs/2604.24832'
citation: 'Yuxiang Wang, et al. "Locality-aware Diffusion Language Modeling." <i>arXiv:2604.24832</i>, 2026.'
---

## Summary

This paper systematically studies *when* and *why* Masked Diffusion Language Models can be trained effectively, contrasting them with autoregressive LLMs across structured generation tasks. The central question: how does the inductive bias of a generative paradigm interact with the dependency structure of the target task?

## Controlled tasks

Three tasks are designed to isolate distinct dependency structures:

- **In-context linear regression** — local exact binding
- **Star-graph path-finding** — reverse planning
- **Sudoku** — global constraint satisfaction

## Methods

Two locality-aware blockwise diffusion architectures are proposed:

- **Scatter** — *intra-block AR + inter-block synchronous update.* Preserves local ordering inside each block while allowing parallel cross-block refinement.
- **Jigsaw** — *intra-block AR + inter-block entropy-guided dynamic programming.* Reconciles local sequential generation with global iterative optimization.

## Key findings

Performance is closely tied to task dependency structure:
- On strongly local-dependency tasks (in-context linear regression), **Jigsaw** dramatically improves convergence and training stability, approaching AR.
- On global-planning / constraint-satisfaction tasks (path-finding, Sudoku), the **Diffusion** paradigm uniformly outperforms AR.

These results suggest AR is the right tool for local-binding sequential generation, while Diffusion is better suited to global planning and constraint satisfaction — providing empirical guidance for dLLM architecture design and downstream Agent-planning research.
