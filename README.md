# Graph Embedding Evaluation

How well do node embeddings keep a graph's community structure? This project compares two embedding methods, HOPE (based on Katz similarity) and Node2Vec, on two synthetic graphs with known communities and on the European high-voltage power grid. It was an assignment for DS8014 (Graph Mining) at Toronto Metropolitan University. All the code is in `analysis.ipynb`.

## How embeddings are judged

Each embedding is evaluated in two ways. The first is the divergence score from the CGE framework (global and local Jensen-Shannon divergence), which checks how well distances in the embedding reflect the graph's community structure, without needing any labels. The second is to cluster the embedded nodes with KMeans and compare the clusters with the true communities using AMI, ARI and a graph-aware agreement measure. UMAP projections to 2D are used to look at the best and worst embeddings side by side.

## Experiments

[ABCD benchmark graphs](abcd-embedding-quality/README.md). ABCD graphs come with planted communities, so embeddings of different methods and dimensions can be compared against a known answer.

[Ring of cliques](ring-of-cliques-embedding-stability/README.md). A small graph of dense cliques joined in a ring. The best and worst embeddings were almost identical in local divergence (about 0.094 vs 0.095), so the embeddings were stable on this kind of graph.

[European power grid](european-grid-embedding-robustness/README.md). The giant component of the European high-voltage grid, a large real infrastructure network. Repeated embeddings were scored the same way, and the best and worst UMAP projections looked similar, so the global structure was preserved consistently.

## Files

`analysis.ipynb` runs all three experiments. The `*.edgelist` and `*.communities` files are the inputs in CGE format, and the `gridkit_europe-highvoltage-*` files are the original grid data from GridKit. Requirements: Python with igraph, networkx, scikit-learn and umap-learn, plus the CGE scripts used in the course.
