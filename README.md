# Shortest Path

In this lab, I addressed the shortest path problem between two cities (nodes), comparing the performance of heuristic and optimized algorithms against a known baseline (NetworkX algorithms).

## Implemented Algorithms

To solve the problem, I distinguished cases based on edge weight types:

### 1. Positive Weights: A* (A-Star)

When `negative_values = False`, I implemented the A* algorithm. A* uses a heuristic (Euclidean distance scaled by 1000) to guide the search toward the target.

### 2. Negative Weights: SPFA (Shortest Path Faster Algorithm)

When `negative_values = True`, A* and Dijkstra are not applicable. I implemented SPFA, an optimized version of Bellman-Ford that uses a queue to process only nodes whose distance has been updated.

## Dataset and Results

For each configuration, a statistical sampling strategy was adopted: 5 random (start, end) pairs were selected.

Larger graph sizes (500 and 1000 nodes) were excluded from the experiments to maintain reasonable computation times.

The final results reported in the CSV were filtered to include only cases where a valid and positive path exists, comparing the cost obtained and nodes visited by my algorithm against the baseline (NetworkX).