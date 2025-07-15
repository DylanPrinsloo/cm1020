# Tree Fundamentals - Lecture Notes

## [Cyclic Graphs](images/acyclic_graph.png)
**Definition**: Graph G is acyclic if it has no cycles, loops, or parallel edges.

```
G₁ (has cycle):     G₂ (acyclic):
B → C               A → B
↑   ↓               ↓   ↓
E ← D               C   D
```

## [Tree Definition](images/defintion_of_a_tree.png)
**Formal definition**: Undirected graph G is a tree if and only if it is:
- **Connected**: Path exists between any two vertices
- **Acyclic**: No cycles

```
G₁ (connected, not tree):  G₂ (tree):      G₃ (tree):
    A                         A               A
   / \                       /               /|\
  B---D                     B               B C D
   \ /                     /                 |  \
    C                     C                  E   F
                         /                      /|\
                        D                      G H I
```

## Forest
**Definition**: Disconnected, cycle-free graph.

```
Forest F:
A---B    C---D---E
    |        |
    F        G
```

## Tree Properties

### Property 1: Unique Path
Every tree has exactly one simple path between any two vertices.

**Proof by contradiction**: If paths P₁ and P₂ exist between vertices B and I, combining P₁ with reverse P₂ creates a cycle, violating tree definition.

### Property 2: Edge Count
Tree with n vertices has exactly (n-1) edges.

**Examples**:
- G₁: 3 vertices, 2 edges
- G₂: 4 vertices, 3 edges
- G₃: 9 vertices, 8 edges

## Rooted Trees
**Definition**: Tree with designated root vertex, all edges directed away from root.

```
Rooted tree:
      Root
     / | \
    A  B  C
   /  /|  \
  D  E F   G
```