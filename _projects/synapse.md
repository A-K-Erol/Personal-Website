---
layout: page
title: Synapse
description: LLM-guided genetic resume optimization for explainable job-person fit
img: assets/img/projects_synapse.png
importance: 2
category: research
---

Synapse is a two-phase retrieval and resume optimization system that improves job-person fit through explainable ranking and LLM-guided genetic evolution of resumes toward target job postings.

**How it works:**
- Phase 1 retrieves candidate job postings using semantic and keyword-based signals
- Phase 2 applies LLM-guided Differential Evolution to iteratively improve resume alignment with target postings, using mutation, crossover, and fitness evaluation operators
- The system surfaces fine-grained skill and keyword alignment explanations at each step

**Key results:**
- Evaluated on CPU (Intel Xeon Gold 6226) and GPU (NVIDIA H100 HGX) backends
- Outperforms traditional keyword-overlap and embedding-only baselines on retrieval quality
- Generates explainable, human-readable rationale for ranking and optimization decisions

**Stack:** Python, LLMs (API), vector retrieval, evolutionary algorithms

**Publication:** Erol, A. K., Yoon, S., Hom, K., & Zhang, X. (2026). *[Synapse: Evolving Job-Person Fit with Explainable Two-phase Retrieval and LLM-guided Genetic Resume Optimization.](https://arxiv.org/abs/2604.02539)* arXiv preprint.
