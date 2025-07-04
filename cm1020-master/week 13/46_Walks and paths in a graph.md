# Graph Theory: Paths, Connectivity, and Special Graph Types

## Types of Vertex-Edge Sequences

### Walk
- **Definition**: A sequence of vertices and edges where both vertices and edges can be repeated
- **Length**: Determined by the number of edges (k edges = walk of length k)
- **Example**: V1 → V2 → V3 → V3 → V4 → V6 using edges e1, e2, e3, e4 (length 4)

```
V1 --e1--> V2 --e2--> V3 --e3--> V4 --e4--> V6
```

### Trail
- **Definition**: A walk where no edge is repeated (vertices can be repeated)
- **Key Feature**: Each edge is traversed at most once
- **Example**: A path using edges e1, e2, e3, e5, e6 without repeating any edge

```
V1 --e1--> V2 --e2--> V3 --e3--> V4 --e5--> V5 --e6--> V6
```

### Circuit
- **Definition**: A closed trail (starts and ends at the same vertex)
- **Key Feature**: No repeated edges, but the starting vertex appears twice (start and end)
- **Example**: A closed path using edges e7, e6, e8, e3, e2, e1

```
V1 --e1--> V2 --e2--> V3 --e3--> V4
^                                |
|                                |
+--e7--> V6 <--e6-- V5 <--e8-----+
```

### [Path](images/4path_and_no_path.png)
- **Definition**: A trail where neither vertices nor edges are repeated
- **Length**: Number of edges contained in the path
- **Example**: V1 → V2 → V3 → V4 → V6 using edges e1, e2, e3, e4 (no repetition)

### [Cycle](images/5cycle.png)
- **Definition**: A closed path where a vertex is reachable from itself
- **Key Feature**: Forms a loop with no repeated vertices except start/end
- **Example**: V1 → V2 → V5 → V1 using edges e1, e2, e3 (length 3)

```
V1 --e1--> V2
^          |
|          |e2
|          v
+--e3-- V5
```

## Historical Context: The Königsberg Bridge Problem

In 1736, residents of Königsberg, Germany wondered if they could walk through the town crossing each of the seven bridges exactly once. **Leonhard Euler** proved this was impossible, creating the foundation of graph theory. He showed that no walk exists that crosses each edge exactly once.

## Special Types of Paths

### [Eulerian Path](images/6eulers_path.png)
- **Definition**: A path that uses each edge of the graph exactly once
- **Traversable Graph**: A graph containing an Eulerian path
- **Example**: A path that visits every edge precisely once

```
Graph with Eulerian Path:
V1 --e1--> V2 --e2--> V3
|          |          |
e7         e6         e3
|          |          |
V4 <--e5-- V5 <--e4-- V6

Eulerian Path: e2→e4→e6→e7→e5→e3→e1
```

### [Hamiltonian Path](images/7hamiltonian_path.png)
- **Definition**: A path that visits each vertex exactly once
- **Traceable Graph**: A graph containing a Hamiltonian path
- **Key Difference**: Focuses on vertices (not edges like Eulerian)

```
V1 ---- V2 ---- V3
|       |       |
V4 ---- V5 ---- V6

Hamiltonian Path: V1→V2→V3→V6→V5→V4 (visits each vertex once)
```

### [Hamiltonian Cycle](images/8hamiltonian_cycle.png)
- **Definition**: A cycle that visits each vertex exactly once, except the starting vertex (visited at start and end)
- **Hamiltonian Graph**: A graph containing a Hamiltonian cycle

```
V1 ---- V2 ---- V3
|               |
V4 ------------ V5

Hamiltonian Cycle: V1→V2→V3→V5→V4→V1
```

## [Graph Connectivity](images/9strong_connectivity_graph.png)

### Connected Graph (Undirected)
- **Definition**: A graph where you can reach any vertex from any other vertex by following edges
- **Property**: Every pair of vertices is connected by at least one path

```
Connected Graph:
V1 ---- V2 ---- V3
|       |       |
V4 ---- V5 ---- V6
```

### Disconnected Graph
- **Definition**: A graph where some vertices cannot reach others
- **Example**: Two separate components with no connecting edges

```
Disconnected Graph:
V1 ---- V2    V3 ---- V4
|       |     |       |
V5 ---- V6    V7 ---- V8
```

### Strongly Connected Digraph
- **Definition**: A directed graph where there exists a directed path between all pairs of vertices
- **Key Feature**: You can reach any vertex from any other vertex following directed edges

```
Strongly Connected Digraph:
V1 ----→ V2
↑        ↓
V4 ←---- V3
```

### Weakly Connected Digraph
- **Definition**: A directed graph that is not strongly connected
- **Example**: Missing directed paths between some vertex pairs

```
Not Strongly Connected:
V1 ----→ V2 ----→ V3
         ↓
         V4
(No path from V4 to other vertices)
```

## [Transitive Closure](images/10transitive_closure.png)

### Definition
Given a digraph G, the **transitive closure** G* is a digraph with:
- Same vertices as G
- A directed edge from U to V if there exists any directed path from U to V in G

### Purpose
Provides **reachability information** - shows which vertices can reach which other vertices.

### Example
Original Graph G:
```
X ----→ Z ----→ U ----→ V
        ↑
Y ------+
```

Directed paths in G:
1. X → Z → U
2. X → Z → U → V  
3. Z → U → V
4. Y → U → V (via Y → Z → U → V)

Transitive Closure G*:
```
X ----→ Z ----→ U ----→ V
|       ↑       ↑       ↑
|       |       |       |
+-------+-------+-------+
        |               |
Y ------+---------------+
```

Additional edges in G*:
- X → U (path X → Z → U exists)
- X → V (path X → Z → U → V exists)
- Z → V (path Z → U → V exists)
- Y → V (path Y → Z → U → V exists)

## Summary

This lecture covered essential graph theory concepts:

1. **Sequence Types**: Walk (allows repetition) → Trail (no edge repetition) → Path (no repetition) → Cycle (closed path)

2. **Special Paths**: 
   - Eulerian (uses each edge once)
   - Hamiltonian (visits each vertex once)

3. **Connectivity**:
   - Connected graphs (undirected)
   - Strongly connected digraphs (directed)

4. **Transitive Closure**: Shows all possible reachability relationships in a directed graph

These concepts form the foundation for analyzing graph structure, pathfinding algorithms, and network connectivity problems in computer science and mathematics.