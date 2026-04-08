# ABCD Synthetic Graph Embedding Quality

## Objective

Evaluate how well HOPE and Node2Vec preserve community structure on controllable synthetic benchmark graphs (ABCD model).

## Approach

- Generated ABCD graphs with predefined community structure.
- Produced embeddings over multiple dimensions.
- Evaluated divergence quality and clustered embeddings with known number of communities.
- Measured clustering recovery via AMI/ARI/AGRI-like metrics.

## Key Outcome

- Established a consistent evaluation framework linking embedding settings (algorithm + dimension) to quantitative community-recovery quality.

## Why this matters

Synthetic benchmarks with known structure are essential for controlled method validation before deployment on real data.

## Reproducibility

See notebook: `../analysis.ipynb` (ABCD embedding section)

