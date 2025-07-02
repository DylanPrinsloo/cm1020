# Graph Theory: Basic Concepts and Definitions

## What is a Graph?

A **graph** is a discrete mathematical structure consisting of **vertices** (nodes) and **edges** (connections) that link these vertices together.

## Formal Definition

A graph **G** can be formally represented as an ordered pair:

**G = (V, E)**

Where:
- **V** is the set of vertices (nodes)
- **E** is the set of edges (connections between vertices)

## Key Components

### Vertices
- **Definition**: The basic elements of a graph, typically drawn as dots or circles
- **Notation**: The set of vertices is denoted as V(G) or simply V
- **Example**: A graph with three vertices would have V = {v₁, v₂, v₃}

```
    v₁
    
v₂     v₃
```

### Edges
- **Definition**: Links or connections between two vertices, drawn as lines
- **Notation**: The set of edges is denoted as E(G) or simply E
- **Example**: A graph with two edges would have E = {e₁, e₂}

```
    v₁
   /  \
  /    \
v₂ ---- v₃
e₁  e₂
```

## Important Relationships

### Adjacency
Two concepts of adjacency exist in graph theory:

1. **Vertex Adjacency**: Two vertices are adjacent if they are connected by the same edge
2. **Edge Adjacency**: Two edges are adjacent if they share a common vertex

### Incidence
A vertex **v** and an edge **e** are **incident** if the vertex is an endpoint of that edge.

## Example Graph Analysis

Consider a graph with:
- **V** = {v₁, v₂, v₃, v₄, v₅, v₆}
- **E** = {e₁, e₂, e₃, e₄, e₅, e₆, e₇}

```
v₁ ---- v₂ ---- v₃
|       |       |
e₇      e₂      e₃
|       |       |
v₆ ---- v₅ ---- v₄
   e₆      e₄
```

In this example:
- v₁ and v₂ are **adjacent** (connected by edge e₁)
- Edges e₁ and e₇ are **adjacent** (both connect to vertex v₁)
- Edge e₁ and vertex v₂ are **incident** (v₂ is an endpoint of e₁)

## Special Edge Types

### Parallel Edges
**Parallel edges** occur when two or more edges connect the same pair of vertices.

```
v₂ ====== v₅
   e₆ e₈
```

In this case, both e₆ and e₈ connect vertices v₂ and v₅.

### Loops
A **loop** is an edge that connects a vertex to itself.

```
v₁ ⟲ e₉
```

Here, edge e₉ forms a loop by connecting v₁ to itself.

## Directed Graphs (Digraphs)

A **directed graph** or **digraph** is a graph where edges have a specific direction, typically indicated by arrows.

```
v₁ ----→ v₂
   e₁

v₂ ⇄ v₅
   e₆ e₈
```

In directed graphs:
- Edge e₁ goes **from** v₁ **to** v₂ (but not the reverse)
- Edge e₆ goes from v₂ to v₅
- Edge e₈ goes from v₅ to v₂
- The direction matters for connectivity and path analysis

## Summary

Graph theory provides a mathematical framework for representing relationships between objects. The fundamental concepts include:

- **Graphs** as collections of vertices and edges
- **Adjacency** relationships between vertices and edges
- **Incidence** relationships between vertices and their connecting edges
- **Special cases** like parallel edges and loops
- **Directed graphs** where edge direction matters

These basic concepts form the foundation for more advanced graph theory topics and have applications in computer science, network analysis, social media, transportation systems, and many other fields.