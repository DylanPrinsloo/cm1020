# Minimum Cost Spanning Trees - Lecture Notes

## Application
**Real-world use**: Connect houses with utilities (power, water, sewage, telephone) at minimum cost.

## Definition
**Weight of spanning tree**: Sum of all edge costs.

**Minimum cost spanning tree**: Spanning tree with lowest total weight.

### Example:
```
Graph G with weights:
    A--8--B--6--C
    |     |     |
    9     5     2
    |     |     |
    D--7--E--4--F
```

- T₁ weight: 8+9+6+7+3 = 33
- T₂ weight: 6+9+5+2+7 = 29  
- T₃ weight: 8+6+4+1+2 = 21
- T₄ (minimum): lowest cost spanning tree

## [Kruskal's Algorithm](images/kruskals_algorithm.png)
**Strategy**: Start with cheapest edge, repeatedly add cheapest edge that doesn't create cycle.

### Steps:
1. Initialize T with all vertices
2. Sort edges by weight
3. Add cheapest edge if no cycle formed
4. Repeat until spanning tree complete

### Example execution:
```
Iteration 1: Add BD (cheapest)
Iteration 2: Add BC  
Iteration 3: Add BF
Iteration 4: Add BA (skip DC - creates cycle)
Iteration 5: Add DE
```

## [Prim's Algorithm](images/prims_algorithim.png)
**Strategy**: Start with any node, repeatedly add cheapest edge to unvisited node.

### Steps:
1. Pick arbitrary starting node (e.g., A)
2. Add cheapest edge to unvisited node
3. Consider all edges from visited nodes
4. Repeat until all nodes included

### Example execution:
```
Start: A
Add: AB (cheapest from A)
Add: BD (cheapest from A,B)
Add: BC (cheapest from A,B,D)
Add: BF (cheapest from A,B,D,C)
Add: DE (cheapest remaining)
```

## Summary
Both algorithms find minimum cost spanning trees but use different approaches:
- **Kruskal's**: Global edge selection, cycle detection
- **Prim's**: Local node expansion, greedy selection