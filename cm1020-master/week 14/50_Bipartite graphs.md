# Bipartite Graphs

## What is a Bipartite Graph?

A bipartite graph is a special type of graph where the vertices can be divided into two disjoint sets (V₁ and V₂) such that every edge connects a vertex in V₁ to a vertex in V₂. No edges exist between vertices within the same set.

### Key Properties

1. **Two-Colorable**: Vertices can be colored using exactly two colors (one color for each set) with no adjacent vertices having the same color.
   
2. **No Odd-Length Cycles**: Bipartite graphs cannot contain cycles of odd length. Adding an edge that creates an odd-length cycle destroys the bipartite property.

## Example of a Bipartite Graph

A graph G with:
- Set V₁ containing vertices {A, B, C, D}
- Set V₂ containing vertices {X, Y, Z}

Each edge connects a vertex from V₁ to a vertex in V₂.

```
    A --- X
    |     |
    B --- Y
    |     |
    C --- Z
    |
    D
```

## Matchings in Bipartite Graphs

### What is a Matching?

A matching is a set of pairwise non-adjacent edges (none of which are loops), meaning no two edges share a common endpoint.

- **Matched/Saturated Vertex**: A vertex that is an endpoint of one of the edges in the matching
- **Unmatched Vertex**: A vertex that is not part of any edge in the matching

### Maximum Matching

A maximum matching is a matching of maximum size such that if any edge is added, it is no longer a matching. It's the largest possible number of edges that can still form a matching.

In a bipartite graph, there might be multiple valid maximum matchings.

## Finding Maximum Matchings: The Hopcroft-Karp Algorithm

The Hopcroft-Karp algorithm is widely used for finding maximum matchings in bipartite graphs.

### Key Concepts

1. **Augmenting Path**: A path that starts on a free (unmatched) node, alternates between unmatched and matched edges, and ends on a free node. Finding these paths allows us to increase the size of our matching.

2. **Breadth-First Search (BFS)**: Traverses the graph level by level.

3. **Depth-First Search (DFS)**: Traverses the graph all the way to a leaf before starting another path.

### Algorithm Overview

The algorithm uses both BFS and DFS to find augmenting paths and increase the matching size until no more augmenting paths can be found.

## 💼 Example Application: Job Matching

Consider a scenario with three job positions and three candidates where edges represent candidates qualified for specific jobs:

```
C₁ --- J₁
|      |
C₂ --- J₂
|      |
C₃ --- J₃
```

The Hopcroft-Karp algorithm finds the maximum matching by:

1. Starting with no matched edges
2. Using BFS to build layered trees from unmatched vertices
3. Using DFS to find augmenting paths
4. Iterating until all possible matches are made

The end result is an optimal assignment where each candidate is matched to a suitable job.

## Key Takeaways

1. Bipartite graphs have vertices that can be divided into two distinct sets
2. They are two-colorable and contain no odd-length cycles
3. A matching is a set of edges where no two share a common endpoint
4. A maximum matching is the largest possible set of edges that forms a matching
5. The Hopcroft-Karp algorithm efficiently finds maximum matchings in bipartite graphs
6. Bipartite matching has practical applications in job assignments and resource allocation

Understanding bipartite graphs and matching algorithms is essential for solving many real-world optimization problems that involve pairing entities from two distinct groups.