# Rooted Trees: Structure, Properties, and Classification

## What Makes a Tree "Rooted"?

Think of a rooted tree as taking an ordinary tree and designating one special vertex as the "root" - imagine picking up a tree by one of its branches so that all the other branches hang downward from that point. This creates a natural hierarchy and direction in our structure.

Formally, a [**rooted tree**](images/theorem_for_rooted_trees.png) is a directed tree with one distinguished vertex r (the root) such that there exists a directed path from r to every other vertex v in the tree. This means information, authority, or structure flows from the root downward to all other vertices.

Here's the key structural property that defines rooted trees: exactly one vertex (the root) has **in-degree zero** (no edges coming into it), while every other vertex has **in-degree one** (exactly one edge coming into it). This creates that characteristic hierarchical flow.

```
    A (root) ← in-degree = 0
   /|\
  B C D ← each has in-degree = 1
 /|   |
E F   G ← each has in-degree = 1
```

## The Family Tree Analogy: [Understanding Terminology](images/terminology_of_rooted_trees.png)

Rooted trees naturally give us a family-like vocabulary that makes the relationships crystal clear. Let me walk you through this terminology using a concrete example:

Consider this rooted tree with root A:
```
      A (root)
     /|\
    B C D
   /|   |\
  E F   G H
```

Here's how the family relationships work:

**Parent and Children**: If there's a directed edge from vertex u to vertex v, then u is the **parent** of v, and v is a **child** of u. In our example, A is the parent of B, C, and D. Meanwhile, B is the parent of E and F.

**Siblings**: Vertices that share the same parent are called **siblings**. So B, C, and D are siblings because they all have A as their parent. Similarly, E and F are siblings with parent B.

**Ancestors and Descendants**: The **ancestors** of a vertex are all the vertices on the path from the root to that vertex (not including the vertex itself). The **descendants** of a vertex include all vertices that can be reached by following directed paths downward from that vertex.

**Internal vs External Nodes**: **Internal nodes** (also called non-leaf nodes) have at least one child, while **external nodes** (or leaves) have no children. In our example, A, B, and D are internal nodes, while C, E, F, G, and H are external nodes.

## Measuring Distance and Height in Trees

Understanding how to measure distances in rooted trees gives us powerful tools for analysis. There are two complementary ways to think about distance:

**Depth (Path Length)**: The **depth** of a vertex is the number of edges from the root down to that vertex. This tells us how "far down" in the hierarchy a vertex sits. 

Using our example:
- A (root) has depth 0
- B, C, D have depth 1  
- E, F, G, H have depth 2

**Height**: The **height** of a vertex is the length of the longest path from that vertex down to any leaf. This tells us how much "tree structure" exists below a given vertex.

From our example:
- Leaves (C, E, F, G, H) have height 0
- B has height 1 (longest path B→E or B→F)
- D has height 1 (longest path D→G or D→H)
- A has height 2 (longest path A→B→E)

The **height of the entire tree** is simply the height of the root vertex, which equals the maximum depth of any vertex in the tree.

## [Special Classes of Rooted Trees](images/special_trees.png)

Understanding these classifications helps us recognize patterns and apply appropriate algorithms:

**Binary Trees**: Every vertex has at most 2 children. These are fundamental in computer science because they naturally model decision processes and hierarchical data structures.

```
    A
   / \
  B   C
 /   / \
D   E   F
```

**Ternary Trees**: Every vertex has at most 3 children. These appear in applications where we have three-way decision points.

[**m-ary Trees**](images/m-ary_tree.png): Every vertex has at most m children. This generalizes our concept to arbitrary branching factors.

**Regular Trees**: An m-ary tree is **regular** if every internal node has exactly m children (not just "at most m"). Regular trees have very predictable structure and growth patterns.

## The Mathematics of Tree Growth

Here's where the structure becomes beautifully predictable. In an m-ary tree, the maximum number of vertices at level h is exactly m^h. Think about why this makes sense: at level 0 (the root), we have 1 = m^0 vertex. At level 1, each root can have at most m children, giving us m^1 vertices. At level 2, each of those m vertices can have at most m children, giving us m^2 vertices, and so on.

This leads to a powerful formula: the maximum total number of vertices in an m-ary tree of height h is:
(m^(h+1) - 1) / (m - 1)

This geometric series formula captures the exponential growth that makes trees such efficient structures for organizing information.

## Isomorphism: When Trees Have the Same Shape

Two trees are **isomorphic** if there exists a bijection (one-to-one correspondence) between their vertex sets that preserves all adjacency relationships. In simpler terms, they have the same "shape" even if their vertices are labeled differently.

[For example](images/example_of_isomorphic.png), these two trees are isomorphic:
```
Tree T1:        Tree T2:
   A               X
  / \             / \
 B   C           Y   Z

Mapping: A↔X, B↔Y, C↔Z preserves all edges
```

However, [**rooted tree isomorphism**](images/example_of_not_isomorphic.png) is more restrictive. Two rooted trees are isomorphic as rooted trees only if there exists an isomorphism that maps the root of one tree to the root of the other tree. This means the hierarchical structure must be preserved exactly.

This distinction is crucial: [two trees might be isomorphic as graphs but not as rooted trees](images/may_or_may_not_be_isomorphic_as_a_rooted.png) if their root positions create different hierarchical structures.

## Why This Matters: The Deep Connection

Rooted trees aren't just abstract mathematical objects - they model hierarchical relationships everywhere around us. Organizational charts, file systems, family trees, decision processes, and parse trees in programming languages all follow rooted tree structures.

The key insight is that by adding direction and designating a root, we transform a symmetric relationship (the undirected tree) into an asymmetric, hierarchical one. This hierarchy gives us natural concepts of "levels," "authority flow," and "structural depth" that mirror how we organize information and relationships in the real world.

Understanding the mathematics of rooted trees - their growth patterns, their classification systems, and their isomorphism properties - gives you a powerful toolkit for analyzing any hierarchical system you encounter. Whether you're designing algorithms, organizing data, or modeling real-world relationships, these concepts provide the theoretical foundation for understanding structure and hierarchy.