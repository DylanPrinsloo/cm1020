# Spanning Trees - Lecture Notes

## Definition
A [**spanning tree**](images/spanning_tree.png) of graph G is a connected, cycle-free subgraph containing all vertices of G.

**Real-world application**: Internet multicasting systems require identifying trees within network graphs.

## Construction Method
1. Keep all vertices of G
2. Remove edges to break all cycles
3. Maintain connectivity

## Examples

### Graph G with 4 spanning trees:
```
Original G:     T₁:        T₂:        T₃:        T₄:
A---B           A---B      A   B      A---B      A   B
|   |           |          |   |      |          |   |
C---D           C---D      C---D      C   D      C---D
```

### [Spanning tree counts:](images/spanning_tree_continued.png)
- G₁: 4 possible spanning trees
- G₂: 8 possible spanning trees  
- G₃: 16 possible spanning trees

## Isomorphic Spanning Trees
Two spanning trees are **isomorphic** if there exists a bijection preserving adjacency between them.

### Example Analysis:
```
Graph G:        T₁:        T₂:        T₃:        T₄:
A---B           A---B      A   B      A---B      A   B
|\ /|           |          |\  |      |          |  /|
| X |           |          | \ |      |          | / |
|/ \|           |          |  \|      |          |/  |
C---D           C---D      C   D      C   D      C   D
```

**Result**: T₁, T₃, and T₄ are isomorphic to each other but non-isomorphic to T₂.

**Practical implication**: When drawing all spanning trees, only non-isomorphic ones need to be shown (e.g., T₁ and T₂).

## Summary
Spanning trees identify essential connectivity within graphs by preserving all vertices while eliminating cycles. Isomorphic analysis reduces redundancy in spanning tree enumeration.