# Graph Embedding Evaluation and Stability Analysis

Primary analysis notebook: `analysis.ipynb`

## Project Overview

This project evaluates graph embeddings for community-structure preservation across synthetic benchmark graphs and real infrastructure graphs.

It compares:
- **HOPE** (Katz similarity)
- **Node2Vec**

and evaluates embedding quality with divergence metrics and clustering recovery.

## Methods and Metrics

- Embedding generation across multiple dimensions
- Divergence evaluation with `CGE` (JSD / local JSD)
- Clustering quality via KMeans on embeddings using:
  - AMI
  - ARI
  - AGRI/GAM-style agreement metric
- 2D projection with UMAP for visual diagnostics

## Why this project is highly relevant

This is the strongest DS/ML portfolio project in the set because it demonstrates:
- representation learning on graphs,
- model comparison and robustness analysis,
- reproducible metric-driven evaluation.

## Subprojects

- [`abcd-embedding-quality`](abcd-embedding-quality/README.md)
- [`ring-of-cliques-embedding-stability`](ring-of-cliques-embedding-stability/README.md)
- [`european-grid-embedding-robustness`](european-grid-embedding-robustness/README.md)


