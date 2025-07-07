# Adjacency Matrix of a Graph: A Comprehensive Summary

## 📊 Graph Representation Methods

There are multiple ways to represent a graph mathematically:

1. **Set representation**: Using a set of vertices V and edges E
2. **Degree sequence**: Listing the degrees of all vertices
3. **Adjacency list**: Listing each vertex with its adjacent vertices
4. **Adjacency matrix**: A square matrix showing connections between vertices

## 🔄 Adjacency Lists

An adjacency list represents a graph by listing each vertex along with all vertices adjacent to it.

### Example:

For a graph with vertices A, B, C, D, and E:

```
A: B, C
B: A, C, D
C: A, B, D, E
D: B, C, E
E: C, D
```

This representation shows that vertex A is adjacent to vertices B and C, vertex B is adjacent to vertices A, C, and D, and so on.

### Creating a Graph from an Adjacency List:

Given an adjacency list:
```
v₁: v₁, v₂, v₃
v₂: v₁, v₄, v₅
v₃: v₁, v₄
v₄: v₂, v₃, v₅
v₅: v₂, v₄
```

We can draw a graph with 5 vertices where each vertex connects to the vertices listed in its adjacency list.

## 🔢 Adjacency Matrices

An adjacency matrix is a square matrix where rows and columns represent vertices. Matrix elements indicate whether pairs of vertices are adjacent.

### Construction Rules:

- For simple graphs: 
  - Matrix element m₍ᵢ,ⱼ₎ = 1 if there is an edge between vertices i and j
  - Matrix element m₍ᵢ,ⱼ₎ = 0 if there is no edge between vertices i and j

- For graphs with loops and parallel edges:
  - Diagonal elements m₍ᵢ,ᵢ₎ represent loops at vertex i
  - Matrix elements > 1 represent multiple parallel edges

### Key Properties:

#### For Undirected Graphs:

1. **Symmetry**: The adjacency matrix is symmetric (m₍ᵢ,ⱼ₎ = m₍ⱼ,ᵢ₎)
2. **Edge Count**: Number of edges = ½ × (sum of all matrix elements)
3. **Degree Relation**: Sum of all matrix elements = sum of the degree sequence

#### Example:
For a graph with vertices v₁, v₂, v₃ with degrees 4, 5, and 3 respectively:
- Sum of degree sequence = 4 + 5 + 3 = 12
- Sum of adjacency matrix elements = 12
- Number of edges = 12 ÷ 2 = 6

#### For Directed Graphs:

1. **Non-symmetric**: The adjacency matrix may not be symmetric
2. **Edge Count**: Number of edges = sum of all matrix elements
3. **Direction**: m₍ᵢ,ⱼ₎ = 1 means there's an edge from i to j

## 🔍 Powers of Adjacency Matrices

The square of an adjacency matrix (M²) reveals the number of paths of length 2 between vertices:

- Element m²₍ᵢ,ⱼ₎ = number of distinct paths of length 2 from vertex i to vertex j

### Example:
For a directed graph with adjacency matrix M, M² shows that:
- From v₁: 1 path of length 2 to v₁, 0 paths to v₂ or v₃
- From v₂: 4 paths of length 2 to v₁, 1 path to v₂, 2 paths to v₃
- From v₃: 1 path of length 2 to v₁, 0 paths to v₂ or v₃

## 🔑 Key Takeaways

1. Adjacency lists provide a space-efficient way to represent sparse graphs
2. Adjacency matrices make it easy to check if two vertices are adjacent
3. For undirected graphs, adjacency matrices are symmetric
4. The sum of matrix elements relates directly to the graph's degree sequence
5. Powers of adjacency matrices reveal path information between vertices

Understanding these representation methods is crucial for implementing efficient graph algorithms and analyzing graph properties in computer science and network theory.