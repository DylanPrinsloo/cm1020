# Properties of Relations

In this lecture, we examine three fundamental properties that relations can possess: reflexivity, symmetry, and antisymmetry. We will define each property formally and explore how these properties manifest in both digraph and matrix representations.

## Reflexivity

### Definition

A relation $R$ on a set $S$ is **reflexive** if and only if:
$$\forall x \in S, \quad x \, R \, x$$

Equivalently, for all $x \in S$, the ordered pair $(x,x) \in R$.

### Examples

**Example 1: Reflexive Relation**

Let $R$ be a relation on $\mathbb{Z}$ defined by:
$$R = \{(a,b) \mid a, b \in \mathbb{Z} \text{ and } a \leq b\}$$

This relation is reflexive because for all $x \in \mathbb{Z}$, we have $x \leq x$, so $(x,x) \in R$.

**Example 2: Non-Reflexive Relation**

Let $R$ be a relation on $\mathbb{Z}$ defined by:
$$R = \{(a,b) \mid a, b \in \mathbb{Z} \text{ and } a < b\}$$

This relation is not reflexive because for any $x \in \mathbb{Z}$, we have $x \not< x$, so $(x,x) \notin R$.

### Exercise

Consider these two relations on $\mathbb{Z}$:

**Relation $R_1$:** $(a,b) \in R_1$ if and only if $a \bmod 2 = b \bmod 2$

**Relation $R_2$:** $(a,b) \in R_2$ if and only if $a - b = 2$

- $R_1$ is reflexive: For any $a \in \mathbb{Z}$, we have $a \bmod 2 = a \bmod 2$, so $(a,a) \in R_1$.
- $R_2$ is not reflexive: For any $a \in \mathbb{Z}$, we have $a - a = 0 \neq 2$, so $(a,a) \notin R_2$.

### Digraph Representation of Reflexive Relations

In the digraph of a reflexive relation $R$ on set $S$:
- **Every vertex has a self-loop**

**Example:** Let $S = \{1, 2, 3, 4\}$ with relation $R$ defined as $\leq$. The digraph shows loops at vertices 1, 2, 3, and 4.

### Matrix Representation of Reflexive Relations

For a reflexive relation $R$ with matrix representation $M_R$:
- **All diagonal entries equal 1:** $M_{ii} = 1$ for all $i$

$$M_R = \begin{pmatrix}
1 & * & * & * \\
* & 1 & * & * \\
* & * & 1 & * \\
* & * & * & 1
\end{pmatrix}$$

**Important:** If any diagonal entry equals 0, the relation is not reflexive.

## Symmetry

### Definition

A relation $R$ on a set $S$ is **symmetric** if and only if:
$$\forall a, b \in S, \quad (a \, R \, b \implies b \, R \, a)$$

Equivalently, $(a,b) \in R \implies (b,a) \in R$.

### Example

Let $R$ be a relation on $\mathbb{Z}$ defined by:
$$R = \{(a,b) \mid a, b \in \mathbb{Z} \text{ and } a \bmod 2 = b \bmod 2\}$$

**Proof of symmetry:**
Let $a, b \in \mathbb{Z}$ and assume $(a,b) \in R$.

Then $a \bmod 2 = b \bmod 2$.

Since equality is commutative, $b \bmod 2 = a \bmod 2$.

Therefore $(b,a) \in R$, proving $R$ is symmetric.

### Digraph Representation of Symmetric Relations

In the digraph of a symmetric relation $R$ on set $S$:
- **No single arrows between distinct vertices**
- Either no connection exists, or there are **parallel edges in both directions**

**Example:** For $S = \{1, 2, 3, 4\}$ with the modular arithmetic relation above:
- No connection between 1 and 2 (different parities)
- Parallel edges between 1 and 3 (both odd)
- Parallel edges between 2 and 4 (both even)

### Matrix Representation of Symmetric Relations

For a symmetric relation $R$ with matrix representation $M_R$:
- **The matrix is symmetric:** $M_{ij} = M_{ji}$ for all $i, j$

$$M_R = \begin{pmatrix}
1 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
1 & 0 & 1 & 0 \\
0 & 1 & 0 & 1
\end{pmatrix}$$

## Antisymmetry

### Definition

A relation $R$ on a set $S$ is **antisymmetric** if and only if:
$$\forall a, b \in S, \quad ((a \, R \, b) \land (b \, R \, a)) \implies a = b$$

In other words, if two distinct elements are related in both directions, they must actually be the same element.

### Example

Let $R$ be a relation on $\mathbb{Z}$ defined by:
$$R = \{(a,b) \mid a, b \in \mathbb{Z} \text{ and } a \leq b\}$$

**Proof of antisymmetry:**
Let $a, b \in \mathbb{Z}$ where $(a,b) \in R$ and $(b,a) \in R$.

Then $a \leq b$ and $b \leq a$.

This implies $a = b$.

Therefore, $R$ is antisymmetric.

### Digraph Representation of Antisymmetric Relations

In the digraph of an antisymmetric relation $R$ on set $S$:
- **No parallel edges between distinct vertices**
- Self-loops are permitted

**Example:** Let $S = \{1, 2, 3, 4\}$ with relation $R$ defined as "divides". The digraph shows single directed edges with no parallel connections between different vertices.

### Matrix Representation of Antisymmetric Relations

For an antisymmetric relation $R$ with matrix representation $M_R$:
- **If $M_{ij} \neq 0$ and $i \neq j$, then $M_{ji} = 0$**

$$M_R = \begin{pmatrix}
1 & 1 & 1 & 1 \\
0 & 1 & 0 & 1 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}$$

## Comprehensive Example

Given the matrix:
$$M_R = \begin{pmatrix}
0 & 1 & 0 \\
1 & 1 & 1 \\
0 & 0 & 1
\end{pmatrix}$$

Determine if $R$ is reflexive, symmetric, or antisymmetric.

**Analysis:**
- **Not reflexive:** $M_{11} = 0$ (diagonal contains a zero)
- **Not symmetric:** $M_{21} = 1$ but $M_{12} = 0$ (matrix not symmetric)
- **Antisymmetric:** For all $i \neq j$ where $M_{ij} \neq 0$, we have $M_{ji} = 0$

## Summary

We have explored three fundamental properties of relations:

1. **Reflexivity:** Every element relates to itself
   - Digraph: Self-loops at all vertices
   - Matrix: All diagonal entries equal 1

2. **Symmetry:** If $a$ relates to $b$, then $b$ relates to $a$
   - Digraph: Parallel edges or no edges between distinct vertices
   - Matrix: Symmetric with respect to main diagonal

3. **Antisymmetry:** No two distinct elements relate to each other bidirectionally
   - Digraph: No parallel edges between distinct vertices
   - Matrix: If $M_{ij} \neq 0$ and $i \neq j$, then $M_{ji} = 0$

These properties form the foundation for understanding more complex relational structures in discrete mathematics.