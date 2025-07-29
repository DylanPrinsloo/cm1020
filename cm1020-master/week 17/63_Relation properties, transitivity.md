# Transitivity and Transitive Closure

In this lecture, we explore the property of transitivity in relations and introduce the concept of transitive closure. We will examine how transitivity manifests in digraph representations and learn how to construct the transitive closure of any given relation.

## Transitivity

### Definition

A relation $R$ on a set $S$ is **transitive** if and only if:
$$\forall a, b, c \in S, \quad ((a \, R \, b) \land (b \, R \, c)) \implies (a \, R \, c)$$

In other words, if $a$ is related to $b$ and $b$ is related to $c$, then $a$ must be related to $c$.

### Examples of Transitive Relations

**Example 1: Less Than or Equal To**

Let $R$ be a relation on $\mathbb{N}$ defined by:
$$R = \{(x,y) \mid x, y \in \mathbb{N} \text{ and } x \leq y\}$$

This relation is transitive because:
- If $x \leq y$ and $y \leq z$, then by the transitivity property of $\leq$, we have $x \leq z$
- Therefore, $(x,y) \in R$ and $(y,z) \in R$ implies $(x,z) \in R$

**Example 2: Ancestor Relation**

Let $R$ be a relation on a set of people defined by:
$$R = \{(a,b) \mid a \text{ is an ancestor of } b\}$$

This relation is transitive because:
- If $a$ is an ancestor of $b$ and $b$ is an ancestor of $c$, then $a$ is an ancestor of $c$
- The ancestral relationship naturally follows the transitive property

### Examples of Non-Transitive Relations

**Example 3: Specific Relation**

Consider the relation $R = \{(2,3), (3,2), (2,2)\}$ on some appropriate set.

This relation is **not transitive** because:
- We have $(3,2) \in R$ and $(2,3) \in R$
- But $(3,3) \notin R$
- Since $3 \, R \, 2$ and $2 \, R \, 3$, transitivity would require $3 \, R \, 3$

## Digraph Analysis of Transitivity

### Identifying Non-Transitive Relations

Consider a relation represented by the following digraph on set $S = \{a, b, c, d\}$:

```
a → b → c → d
```

This relation is **not transitive** because:
1. $a \, R \, b$ and $b \, R \, c$, but $a \not R \, c$
2. $b \, R \, c$ and $c \, R \, d$, but $b \not R \, d$

### Visual Test for Transitivity

In a digraph, a relation fails to be transitive when there exists a path of length 2 (two consecutive edges) without a corresponding direct edge. Specifically, if there's a path $x \to y \to z$ but no direct edge $x \to z$, the relation is not transitive.

## Transitive Closure

### Definition

The **transitive closure** of a relation $R$ on set $S$ is the smallest transitive relation $R^+$ that contains $R$. It is obtained by adding the minimum number of ordered pairs to $R$ to make it transitive.

Formally:
$$R^+ = R \cup \{(a,c) \mid \exists b \in S \text{ such that } (a,b) \in R \text{ and } (b,c) \in R\} \cup \ldots$$

### Constructing Transitive Closure

**Step-by-Step Process:**

Given the digraph: $a \to b \to c \to d$

**Step 1:** Identify missing transitive connections
- $a \to b$ and $b \to c$ exist, but $a \to c$ is missing
- $b \to c$ and $c \to d$ exist, but $b \to d$ is missing

**Step 2:** Add the first level of missing edges
- Add edge $(a,c)$
- Add edge $(b,d)$

Current state: $a \to b \to c \to d$ with additional edges $a \to c$ and $b \to d$

**Step 3:** Check for new transitive requirements
- Now $a \to c$ and $c \to d$ exist, but $a \to d$ is missing

**Step 4:** Add remaining missing edges
- Add edge $(a,d)$

**Final Result:** The transitive closure includes all original edges plus:
- $(a,c)$
- $(b,d)$  
- $(a,d)$

### Matrix Representation of Transitive Closure

If $M_R$ represents the original relation, the transitive closure can be computed using:
$$M_{R^+} = M_R \vee M_R^2 \vee M_R^3 \vee \ldots \vee M_R^n$$

where $M_R^k$ represents the $k$-th Boolean power of matrix $M_R$, and $n = |S|$.

### Algorithm for Finding Transitive Closure

**Warshall's Algorithm:**

```
For k = 1 to n:
    For i = 1 to n:
        For j = 1 to n:
            M[i][j] = M[i][j] ∨ (M[i][k] ∧ M[k][j])
```

This algorithm systematically adds all necessary transitive connections by considering each vertex as an intermediate point.

## Properties of Transitive Relations

### Theorem
If $R$ is transitive, then $R^n \subseteq R$ for all positive integers $n$, where $R^n$ denotes the $n$-th composition of $R$ with itself.

### Closure Properties
- The transitive closure $R^+$ is always transitive
- $R^+ = R \cup R^2 \cup R^3 \cup \ldots$
- If $R$ is already transitive, then $R^+ = R$

## Applications

Transitive closure finds applications in:

1. **Graph Theory:** Finding reachability in directed graphs
2. **Database Systems:** Computing ancestor-descendant relationships
3. **Program Analysis:** Determining data dependencies
4. **Social Networks:** Identifying indirect connections

## Summary

In this lecture, we explored:

1. **Transitivity Definition:** A relation where indirect connections through intermediaries create direct connections

2. **Digraph Recognition:** Transitive relations have no "missing links" - every path of length 2 has a corresponding direct edge

3. **Transitive Closure Construction:** The systematic process of adding minimum necessary edges to make a relation transitive

4. **Computational Methods:** Matrix-based approaches and Warshall's algorithm for efficiently computing transitive closures

Transitivity is a fundamental concept that bridges the gap between local pairwise relationships and global connectivity patterns in mathematical structures.