# Graph Theory: Simple, Regular, and Complete Graphs

## Simple Graphs

### Definition
A **simple graph** is a graph that contains:
- **No loops** (edges connecting a vertex to itself)
- **No parallel edges** (multiple edges between the same pair of vertices)

### Examples

**G1 - Simple Graph:**
```
A ---- B
|      |
|      |
C ---- D
```
✓ No loops, no parallel edges

**G2 - Not Simple (Parallel Edges):**
```
A ====== B
   ||
   CD
```
✗ Contains parallel edges between A and B

**G3 - Not Simple (Contains Loop):**
```
A ---- B
⟲     |
|      |
C ---- D
```
✗ Contains a loop at vertex A

### Key Property of Simple Graphs
In a simple graph G with n vertices, **the degree of each vertex is at most n-1**.

**Proof:** A vertex v can connect to at most n-1 other vertices. If degree(v) > n-1, then v must have either loops or parallel edges, contradicting the definition of a simple graph.

### Example Analysis
Simple graph with 4 vertices:
```
    A (degree 3)
   /|\
  / | \
 B--+--C
    |
    D
```
Vertex A has degree 3, which equals n-1 = 4-1 = 3. Adding any more edges would require loops or parallel edges.

## Constructing Simple Graphs from Degree Sequences

### Question: Can we construct simple graphs with these degree sequences?

**Case 1: (4, 2, 2, 2)**
- Sum = 4 + 2 + 2 + 2 = 10 (even) ✓
- Graph is constructible, but can it be simple?
- One vertex has degree 4, but there are only 3 other vertices
- **Answer: NO** - would require loops or parallel edges

**Case 2: (4, 3, 3, 2, 2)**
- Sum = 4 + 3 + 3 + 2 + 2 = 14 (even) ✓
- 5 vertices total, highest degree is 4 < 5-1 ✓
- **Answer: YES** - simple graph possible

```
Constructed graph:
A (deg 4) ---- B (deg 3)
|\            /|
| \          / |
|  C (deg 3)   |
|  |          |
|  |          |
D--+----------E
(deg 2)    (deg 2)
```

## Regular Graphs

### Definition
A graph is **r-regular** if all vertices have the same degree r.

### Examples of Regular Graphs

**1-Regular Graph (2 vertices):**
```
A ---- B
Degree sequence: (1, 1)
```

**2-Regular Graph (3 vertices):**
```
A ---- B
|     /
|    /
|   /
C --+
Degree sequence: (2, 2, 2)
```

**3-Regular Graph (4 vertices):**
```
A ---- B
|\    /|
| \  / |
|  \/  |
|  /\  |
| /  \ |
C ---- D
Degree sequence: (3, 3, 3, 3)
```

### Properties of r-Regular Graphs

For an r-regular graph G with n vertices:

1. **Degree sequence**: (r, r, r, ..., r) [n times]
2. **Sum of degrees**: r × n
3. **Number of edges**: (r × n) ÷ 2

### Example: 3-Regular Graph with 6 Vertices
```
Sum of degrees = 3 × 6 = 18
Number of edges = 18 ÷ 2 = 9
```

### Special Case: Cycles as Regular Graphs

**Cycles are 2-regular graphs:**
- **C₃** (triangle): 3 vertices, degree sequence (2, 2, 2)
- **C₄** (square): 4 vertices, degree sequence (2, 2, 2, 2)  
- **C₅** (pentagon): 5 vertices, degree sequence (2, 2, 2, 2, 2)

```
C₃:     C₄:        C₅:
A       A ---- B    A ---- B
|\     |      |   /      |
| \    |      |  /       |
B--C   D ---- C A        E
                \       /
                 \     /
                  D---C
```

### Constructibility Questions

**Can we construct a 3-regular graph with 4 vertices?**
- Sum of degrees = 3 × 4 = 12 (even) ✓
- **Answer: YES** (shown in example above)

**Can we construct a 3-regular graph with 5 vertices?**
- Sum of degrees = 3 × 5 = 15 (odd) ✗
- **Answer: NO** - sum must be even

## Complete Graphs

### Definition
A **complete graph** is a simple graph where every pair of vertices is adjacent (connected by an edge).

**Notation**: Kₙ represents a complete graph with n vertices.

### Examples of Complete Graphs

**K₁** (1 vertex):
```
A
```

**K₂** (2 vertices):
```
A ---- B
```

**K₃** (3 vertices):
```
A ---- B
 \    /
  \  /
   C
```

**K₄** (4 vertices):
```
A ---- B
|\    /|
| \  / |
|  \/  |
|  /\  |
| /  \ |
C ---- D
```

**K₅** (5 vertices):
```
    A
   /|\
  / | \
 B--+--C
 |\ |/|
 | \|/ |
 |  E  |
 |  |  |
 D--+--+
```

### Properties of Complete Graphs

For a complete graph Kₙ with n vertices:

1. **Degree of each vertex**: n - 1
2. **Sum of degree sequence**: n × (n - 1)
3. **Number of edges**: n × (n - 1) ÷ 2

### Example: K₅ Analysis
- **Vertices**: 5
- **Degree of each vertex**: 5 - 1 = 4
- **Sum of degrees**: 5 × 4 = 20
- **Number of edges**: 20 ÷ 2 = 10

### Formula Derivation
The number of edges in Kₙ can also be derived using combinations:
- We need to choose 2 vertices from n vertices to form an edge
- Number of ways = C(n,2) = n!/(2!(n-2)!) = n(n-1)/2

## Relationships Between Graph Types

### Hierarchy
```
All Graphs
    ↓
Simple Graphs (no loops, no parallel edges)
    ↓
Regular Graphs (all vertices same degree)
    ↓
Complete Graphs (every pair connected)
```

### Special Cases
- **Complete graphs are always regular**: Kₙ is (n-1)-regular
- **Cycles are regular but not complete** (except C₃ = K₃)
- **Regular graphs are not necessarily complete**

## Summary

This lecture covered three important classes of graphs:

1. **Simple Graphs**:
   - No loops or parallel edges
   - Maximum degree = n-1 for n vertices
   - Foundation for other graph types

2. **Regular Graphs**:
   - All vertices have the same degree
   - r-regular means degree = r for all vertices
   - Sum of degrees = r × n must be even

3. **Complete Graphs**:
   - Every pair of vertices is connected
   - Kₙ has n(n-1)/2 edges
   - Each vertex has degree n-1
   - Represents maximum connectivity

These graph types form a hierarchy and are fundamental in graph theory, with applications in network design, social networks, and combinatorial optimization.