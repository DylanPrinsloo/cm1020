# Graph Theory: Vertex Degrees and Degree Sequences

## Vertex Degree

### Definition (Undirected Graphs)
The **degree** of a vertex in a graph is the number of edges incident to (connected to) that vertex.

### Special Cases
- **Loop**: An edge that connects a vertex to itself contributes **2** to the degree
- **Isolated vertex**: A vertex with no connections has degree **0**

### Counting Method
To count the degree of a vertex, draw a circle around it and count how many edges cross the circle.

### Example: Undirected Graph
```
    v2 (degree 2)
    |
v1--+--v3 (degree 4)
|   |  |\
|   |  | \
v6  +--v4-+
(degree 0) (degree 3)
    |
    v5 (degree 1)
```

**Degrees:**
- v1: degree 4
- v2: degree 2  
- v3: degree 4
- v4: degree 3
- v5: degree 1
- v6: degree 0 (isolated)

## Directed Graph Degrees

For directed graphs, we distinguish three types of degrees:

### In-Degree
The number of edges for which the vertex is the **terminal vertex** (edges pointing TO the vertex).

### Out-Degree  
The number of edges for which the vertex is the **initial vertex** (edges pointing FROM the vertex).

### Total Degree
**Degree = In-degree + Out-degree**

### Loop in Directed Graphs
A loop contributes **1** to both in-degree and out-degree, so it contributes **2** to the total degree.

### Example: Directed Graph
```
v1 ←--→ v2
↓  ⟲   ↓
v4 ←--- v3
↓       ↑
v5      |
        v6 (isolated)
```

**Degree Analysis:**
- **v1**: in-degree = 2, out-degree = 2, total degree = 4
- **v2**: in-degree = 1, out-degree = 1, total degree = 2  
- **v3**: in-degree = 2, out-degree = 2, total degree = 4
- **v4**: in-degree = 1, out-degree = 2, total degree = 3
- **v5**: in-degree = 1, out-degree = 0, total degree = 1
- **v6**: in-degree = 0, out-degree = 0, total degree = 0

## Degree Sequence

### Definition
The **degree sequence** of an undirected graph G is a sequence of the degrees of all vertices written in **descending order**, separated by commas.

### Example
For a graph with vertices having degrees 4, 2, 3, 2, 1:
**Degree sequence = (4, 3, 2, 2, 1)**

```
Graph example:
v1 (degree 4) ---- v2 (degree 2)
|    \             |
|     \            |
v5    v3 --------- v4
(degree 1) (degree 3) (degree 2)
```

## Properties of Degree Sequences

### Property 1: Sum is Always Even
**The sum of all degrees in any graph is always even.**

**Proof concept**: Each edge contributes exactly 2 to the total sum (1 for each endpoint), so the sum must be even.

### Property 2: Handshaking Lemma
**Sum of degrees = 2 × Number of edges**

Or equivalently: **Number of edges = (Sum of degrees) ÷ 2**

### Example Verification
Consider a graph with degree sequence (4, 3, 3, 2, 1, 1):

```
Sum = 4 + 3 + 3 + 2 + 1 + 1 = 14 (even ✓)
Number of edges = 14 ÷ 2 = 7 edges
```

Counting edges in the graph confirms 7 edges.

### Another Example
Triangle graph with degree sequence (2, 2, 2):

```
v1 ---- v2
 \     /
  \   /
   v3

Sum = 2 + 2 + 2 = 6 (even ✓)
Number of edges = 6 ÷ 2 = 3 edges ✓
```

## Constructibility of Degree Sequences

### Rule
A degree sequence can represent a valid graph **if and only if** the sum of degrees is even.

### Practice Exercise
Determine which degree sequences can construct valid graphs:

**1. Degree sequence: (3, 2, 2, 1)**
- Sum = 3 + 2 + 2 + 1 = 8 (even)
- **Valid graph possible** ✓
- Number of edges = 8 ÷ 2 = 4

**2. Degree sequence: (3, 3, 2, 1)**  
- Sum = 3 + 3 + 2 + 1 = 9 (odd)
- **No valid graph possible** ✗

## Applications and Significance

### Graph Representation
Degree sequences provide a compact way to represent certain properties of graphs without drawing them.

### Graph Analysis
- **Connectivity**: Degree sequences help analyze how well-connected a graph is
- **Network Analysis**: In social networks, degree represents the number of connections a person has
- **Algorithm Design**: Many graph algorithms use vertex degrees for optimization

### Real-World Examples
- **Social Networks**: Degree = number of friends/followers
- **Computer Networks**: Degree = number of connections to other computers  
- **Transportation**: Degree = number of routes from a location
- **Biology**: Degree = number of interactions for a protein/gene

## Summary

This lecture covered:

1. **Vertex Degrees**: Number of incident edges (loops count twice)
2. **Directed Graph Degrees**: In-degree, out-degree, and total degree
3. **Degree Sequences**: Ordered list of vertex degrees in descending order
4. **Key Properties**:
   - Sum of degrees is always even
   - Sum of degrees equals twice the number of edges
5. **Constructibility**: A degree sequence represents a valid graph only if its sum is even

These concepts are fundamental for understanding graph structure and are essential for more advanced topics in graph theory and network analysis.