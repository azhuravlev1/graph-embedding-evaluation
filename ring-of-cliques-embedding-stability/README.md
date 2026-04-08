# Ring-of-Cliques Embedding Stability Study

## Objective

Assess embedding robustness on a small but structured graph where local communities (cliques) are linked in a ring topology.

## Approach

- Generated ring-of-cliques graph.
- Evaluated multiple embeddings and identified best/worst by divergence.
- Used UMAP to visualize community separation behavior.

## Key Finding

- Best and worst embeddings were very close in JSD (approximately `0.0943` vs `0.0950` local value in the notebook output), suggesting stable behavior on this graph class.

## Why this matters

Stability analysis helps determine whether embedding methods are reliable or highly sensitive to minor configuration changes.

## Reproducibility

See notebook: `../analysis.ipynb` (ring-of-cliques section)

