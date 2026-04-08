# European Power Grid Embedding Robustness

## Objective

Test embedding behavior on a large real-world infrastructure graph (European high-voltage power grid giant component).

## Approach

- Built graph and extracted giant component.
- Created CGE input files (`grid.edgelist`, `grid.communities`).
- Generated repeated embeddings and tracked quality metrics.
- Visualized best/worst embedding projections with UMAP.

## Key Insight

- The notebook indicates relatively close best/worst projection behavior, suggesting non-trivial robustness in preserving global structure on this network.

## Why this matters

Demonstrates transition from synthetic benchmark evaluation to real-world infrastructure data, which is critical for practical analytics credibility.

## Reproducibility

See notebook: `../analysis.ipynb` (European grid section)

