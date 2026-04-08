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
- Weighted-average rank ensemble achieves **nDCG@10 of 0.714**, a **+31.9%** improvement over the embedding-only baseline (0.541)
- Contrastive learning reranker alone yields +17.4% nDCG@10; LLM pairwise ranking adds +10.2%
- GPU (H100) accelerates Phase II scoring **22× over CPU** (0.026s vs. 0.570s per query)
- LLM-guided evolutionary resume optimization achieves a **median 62%, mean 68%, upper-quartile 92%** fitness gain over 5 generations across 100 resumes
- Corpus: 120,000 LinkedIn job postings; 2,500 LiveCareer candidate resumes

**Stack:** Python, LLMs (API), vector retrieval, evolutionary algorithms

**Publication:** Erol, A. K., Yoon, S., Hom, K., & Zhang, X. (2026). *[Synapse: Evolving Job-Person Fit with Explainable Two-phase Retrieval and LLM-guided Genetic Resume Optimization.](https://arxiv.org/abs/2604.02539)* arXiv preprint.
