# Representation of Relations

In this lecture, we explore different methods for representing mathematical relations. We will examine two primary approaches: matrix representation and directed graph (digraph) representation, along with operations on these representations.

## Matrix Representation of Relations

### Definition

Given a relation $R$ from set $A$ to set $B$, we can represent $R$ using a matrix. First, we order the elements of both sets (typically in ascending order, though any consistent ordering works).

Let $|A| = n_a$ and $|B| = n_b$ denote the cardinalities of sets $A$ and $B$ respectively.

The **matrix representation** $M_R$ of relation $R$ is an $n_a \times n_b$ matrix where:

$$M_{ij} = \begin{cases} 
1 & \text{if } a_i \, R \, b_j \\
0 & \text{otherwise}
\end{cases}$$

where $a_i \in A$ and $b_j \in B$.

### Example 1: Student Enrollment

Let $A = \{\text{Sofia}, \text{Samir}, \text{Sarah}\}$ be the set of students, and $B = \{\text{CS100}, \text{CS101}, \text{CS102}, \text{CS103}\}$ be the set of courses.

Define relation $R$ as "is enrolled in". The matrix representation captures which students are enrolled in which courses:

$$M_R = \begin{pmatrix}
1 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
1 & 1 & 0 & 0
\end{pmatrix}$$

where rows represent students and columns represent courses.

### Example 2: Strict Ordering

Let $A = \{1, 2, 3, 4, 5\}$ and define $R$ as the "strictly less than" relation on $A$.

$$R = \{(x,y) \mid x, y \in A \text{ and } x < y\}$$

The matrix representation is:

$$M_R = \begin{pmatrix}
0 & 1 & 1 & 1 & 1 \\
0 & 0 & 1 & 1 & 1 \\
0 & 0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 & 0
\end{pmatrix}$$

Note that the main diagonal contains all zeros since no element is strictly less than itself.

### Example 3: Non-strict Ordering

Using the same set $A = \{1, 2, 3, 4, 5\}$, define $S$ as the "less than or equal to" relation:

$$S = \{(x,y) \mid x, y \in A \text{ and } x \leq y\}$$

The matrix representation is:

$$M_S = \begin{pmatrix}
1 & 1 & 1 & 1 & 1 \\
0 & 1 & 1 & 1 & 1 \\
0 & 0 & 1 & 1 & 1 \\
0 & 0 & 0 & 1 & 1 \\
0 & 0 & 0 & 0 & 1
\end{pmatrix}$$

Here, the main diagonal contains all ones since every element is less than or equal to itself.

## Combining Relations Using Matrices

We can combine relations using Boolean matrix operations, where entries are restricted to $\{0, 1\}$.

### Union of Relations

The **union** of two relations $R$ and $S$ is:
$$R \cup S = \{(a,b) \mid (a,b) \in R \text{ or } (a,b) \in S\}$$

In matrix form, this corresponds to the **join** operation:
$$M_{R \cup S} = M_R \vee M_S$$

where $(M_R \vee M_S)_{ij} = M_R^{(ij)} \vee M_S^{(ij)} = \max(M_R^{(ij)}, M_S^{(ij)})$.

### Intersection of Relations

The **intersection** of two relations $R$ and $S$ is:
$$R \cap S = \{(a,b) \mid (a,b) \in R \text{ and } (a,b) \in S\}$$

In matrix form, this corresponds to the **meet** operation:
$$M_{R \cap S} = M_R \wedge M_S$$

where $(M_R \wedge M_S)_{ij} = M_R^{(ij)} \wedge M_S^{(ij)} = \min(M_R^{(ij)}, M_S^{(ij)})$.

## Directed Graph Representation

### Definition

A relation $R$ on set $A$ can be represented as a **directed graph** (digraph) where:
- Each element of $A$ is a vertex
- There is a directed edge from vertex $x$ to vertex $y$ if and only if $x \, R \, y$

### Example 1: Divisibility Relation

Let $A = \{1, 2, 3, 4\}$ and define relation $R$ as "divides":
$$R = \{(x,y) \mid x, y \in A \text{ and } x \text{ divides } y\}$$

The digraph representation shows:
- Self-loops at every vertex (since every number divides itself)
- Edge from 1 to all other vertices (since 1 divides all numbers)
- Edge from 2 to 4 (since 2 divides 4)

### Example 2: Less Than or Equal To

For $A = \{1, 2, 3, 4, 5\}$ with relation $R$ defined as $x \leq y$:

The digraph contains:
- Self-loops at every vertex (reflexive property)
- Directed edges from each element to all elements greater than or equal to it

### Example 3: Strictly Less Than

Using the same set $A$ with relation $R$ defined as $x < y$:

The digraph differs from the previous example by having:
- No self-loops (since $x \not< x$ for any $x$)
- Directed edges only to strictly greater elements

## Summary

This lecture presented two fundamental methods for representing relations:

1. **Matrix Representation**: Using Boolean matrices where entry $(i,j)$ indicates whether element $i$ is related to element $j$
2. **Digraph Representation**: Using directed graphs where vertices represent elements and edges represent relationships

We also explored how to combine relations using Boolean matrix operations (join for union, meet for intersection) and visualized various types of relations including divisibility, ordering, and strict ordering through both matrix and digraph representations.