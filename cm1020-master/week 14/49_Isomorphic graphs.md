# Graph Isomorphism

## 📊 What is Graph Isomorphism?

Graph isomorphism is a concept that identifies when two graphs are structurally identical, even if they appear different visually. Think of it as recognizing that two graphs are essentially the "same graph" drawn differently.

### Formal Definition

Two graphs G₁ and G₂ are **isomorphic** if there exists a bijection (one-to-one correspondence) f: V(G₁) → V(G₂) that preserves adjacency relationships:

$$\text{For any vertices } u,v \in V(G_1): \{u,v\} \in E(G_1) \Leftrightarrow \{f(u),f(v)\} \in E(G_2)$$

In simpler terms:
- u and v are adjacent in G₁ if and only if f(u) and f(v) are adjacent in G₂
- The function f maps each vertex of G₁ to exactly one vertex of G₂
- Every vertex in G₂ is mapped from exactly one vertex in G₁

## 🔄 Example of Isomorphic Graphs

Consider two graphs G₁ and G₂ where:
- G₁ has vertices {a₁, a₂, a₃, a₄, a₅}
- G₂ has vertices {b₁, b₂, b₃, b₄, b₅}

We can prove they're isomorphic by defining a mapping function f where:
```
f(a₁) = b₁
f(a₂) = b₂
f(a₃) = b₃
f(a₄) = b₄
f(a₅) = b₅
```

This function f is bijective and preserves all adjacency relationships between the graphs.

## ✅ Properties of Isomorphic Graphs

### 1. Degree Sequence Requirement

**Property**: Two graphs with different degree sequences cannot be isomorphic.

**Example**: 
- Graph 1: Degree sequence [3,3,3,1]
- Graph 2: Degree sequence [4,4,3,1]

These graphs cannot be isomorphic because their degree sequences differ.

### 2. Same Degree Sequence ≠ Isomorphism

**Property**: Having the same degree sequence is necessary but not sufficient for isomorphism.

**Example**: 
- Two graphs both with degree sequence [4,2,2,1,1,1,1]
- Yet they're not isomorphic (cannot create a bijection that preserves adjacency)

### 3. Examples of Isomorphic Graph Classes

**2-regular graphs**: All 2-regular, simple, connected graphs with 4 vertices are isomorphic to each other.

```
    A---B        E---F        I---J
    |   |   ≅    |   |   ≅    |   |
    D---C        H---G        L---K
```

**3-regular graphs**: All 3-regular (cubic), simple, connected graphs with 6 vertices are isomorphic.

**2-regular with 5 vertices**: All 2-regular, simple, connected graphs with 5 vertices (cycles C₅) are isomorphic.

```
    A---B            F---G
   /     \          /     \
  E       C   ≅    J       H
   \     /          \     /
    D---E            I---H
```

## 🔑 Key Takeaways

1. Graph isomorphism identifies structurally equivalent graphs
2. Isomorphic graphs must have identical degree sequences (necessary but not sufficient)
3. A bijective function that preserves adjacency proves isomorphism
4. Regular graphs of the same size and degree are often isomorphic
5. Testing for isomorphism often requires checking if adjacency can be preserved while mapping vertices

Understanding graph isomorphism helps recognize when different-looking graphs are structurally the same, which is crucial in algorithm design, network analysis, and computational complexity theory.