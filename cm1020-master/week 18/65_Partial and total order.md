# Partial Orders and Total Orders: Complete Study Notes

## Building on Equivalence Relations: A New Kind of Structure

Now that we understand equivalence relations (which capture the idea of "sameness"), we turn to **ordering relations** that capture the fundamental concept of "comparison" or "precedence." These relations help us understand hierarchical structures and rankings in mathematics and computer science.

## Partial Orders: Formalizing Hierarchical Relationships

### Core Definition and Intuition

A **partial order** is a relation that captures the essence of "less than or equal to" relationships, but in a more general setting than just numbers. Think of it as a way to establish a consistent hierarchy where some elements can be compared, but not necessarily all pairs of elements.

### Formal Definition

Let $R$ be a relation on a set $S$. Then $R$ is a **partial order** if and only if $R$ satisfies these three properties:

1. **Reflexive**: For all $a \in S$, we have $aRa$ (every element is related to itself)
2. **Antisymmetric**: For all $a, b \in S$, if $aRb$ and $bRa$, then $a = b$ (if two distinct elements are mutually related, they must actually be the same element)
3. **Transitive**: For all $a, b, c \in S$, if $aRb$ and $bRc$, then $aRc$ (the ordering chains consistently)

### Understanding Antisymmetry vs. Symmetry

This is where partial orders differ fundamentally from equivalence relations. While equivalence relations are **symmetric** (if $aRb$ then $bRa$), partial orders are **antisymmetric** (if $aRb$ and $bRa$, then $a = b$).

Think about this intuitively: if $a \leq b$ and $b \leq a$, then we must have $a = b$. Two distinct elements cannot both be "less than or equal to" each other unless they're actually the same element.

## [Example 1: The Standard "Less Than or Equal" Relation](images/partial_order_example_one.png)

Consider the relation $R$ on $\mathbb{Z}$ where $(a,b) \in R$ if and only if $a \leq b$.

**Verification that this is a partial order:**

- **Reflexive**: For any $a \in \mathbb{Z}$, clearly $a \leq a$ ✓
- **Antisymmetric**: If $a \leq b$ and $b \leq a$, then we must have $a = b$ ✓
- **Transitive**: If $a \leq b$ and $b \leq c$, then $a \leq c$ ✓

This relation creates a total hierarchy of integers: $\ldots < -2 < -1 < 0 < 1 < 2 < \ldots$

## [Example 2: The Divisibility Relation](images/partial_order_example_two.png)

Consider the relation $R$ on $\mathbb{Z}^+$ (positive integers) where $(a,b) \in R$ if and only if $a$ divides $b$, written as $a \mid b$.

**Verification that this is a partial order:**

- **Reflexive**: Every positive integer $a$ divides itself: $a \mid a$ since $a = a \cdot 1$ ✓
- **Antisymmetric**: If $a \mid b$ and $b \mid a$, then $a = b$. Here's why: if $a \mid b$, then $b = ka$ for some integer $k \geq 1$. If $b \mid a$, then $a = \ell b$ for some integer $\ell \geq 1$. Substituting: $a = \ell(ka) = k\ell a$, which means $k\ell = 1$. Since $k, \ell \geq 1$, we must have $k = \ell = 1$, so $a = b$ ✓
- **Transitive**: If $a \mid b$ and $b \mid c$, then $a \mid c$. If $b = ka$ and $c = \ell b$, then $c = \ell(ka) = (k\ell)a$, so $a \mid c$ ✓

This creates a more complex hierarchy. For example: $1 \mid 2 \mid 4 \mid 8 \mid 16 \mid \ldots$ and $1 \mid 3 \mid 6 \mid 12 \mid \ldots$

## The Crucial Insight: Comparability

Here's where things get interesting. In the divisibility relation, we can compare some pairs of elements (like 2 and 4, since $2 \mid 4$), but we cannot compare others (like 3 and 5, since neither divides the other). This leads us to the concept of **total orders**.

## Total Orders: When Everything Can Be Compared

### Definition and Intuition

A **total order** (also called a **linear order**) is a partial order with an additional crucial property: every pair of elements can be compared.

### Formal Definition

Let $R$ be a relation on a set $S$. Then $R$ is a **total order** if and only if:

1. $R$ is a partial order (reflexive, antisymmetric, and transitive)
2. **Comparable**: For all $a, b \in S$, either $aRb$ or $bRa$ (or both, which by antisymmetry means $a = b$)

The comparability property is sometimes called **trichotomy**: for any two elements $a$ and $b$, exactly one of these must be true: $a < b$, $a = b$, or $a > b$.

## [Example: Standard Ordering is Total](images/total_order_example_one.png)

The relation $R$ on $\mathbb{Z}$ where $aRb$ means $a \leq b$ is a total order because:

1. It's a partial order (as we showed earlier)
2. For any two integers $a$ and $b$, either $a \leq b$ or $b \leq a$ (or both if $a = b$)

This creates a complete linear arrangement of all integers.

## [Example: Divisibility is Only Partial](images/not_total_order_example_two.png)

The divisibility relation on $\mathbb{Z}^+$ is a partial order but **not** a total order because:

1. It's a partial order (as we showed earlier)
2. But some elements are incomparable: neither $5 \mid 7$ nor $7 \mid 5$

Since we cannot compare every pair of elements, this ordering is only partial, not total.

## Visualizing Order Relations

Think of partial orders as creating a **directed acyclic graph** (DAG) where edges represent the ordering relation. In a total order, this DAG is simply a straight line. In a partial order that's not total, you get a more complex branching structure with some elements that cannot be reached from others.

For the divisibility relation on $\{1, 2, 3, 4, 6, 12\}$:
```
      12
     /  \
    4    6
   /    / \
  2    2   3
   \  /   /
    1----
```

Some elements (like 4 and 3) sit on different "branches" and cannot be compared.

## Deep Connections: Why These Matter in Computer Science

Understanding partial and total orders is crucial for several reasons:

**Sorting Algorithms**: Total orders allow us to sort elements completely. Partial orders tell us when complete sorting is impossible, but we can still find valid topological orderings.

**Database Theory**: Partial orders appear in database normalization and dependency relationships between attributes.

**Program Analysis**: Control flow graphs and data dependencies often form partial orders, helping us understand when operations can be performed in parallel versus when they must be sequential.

**Type Systems**: Subtyping relationships in programming languages typically form partial orders, where some types can be compared (one is a subtype of another) while others cannot.

## Developing Your Mathematical Intuition

As you work through problems involving ordering relations, I encourage you to develop a systematic approach to thinking about these concepts. Start by asking yourself whether you can compare every pair of elements in your set. If the answer is yes, you might be dealing with a total order, which means you can arrange all elements in a single, unambiguous sequence. If the answer is no, you're working with a partial order, which creates a more complex hierarchical structure where some elements exist on different "levels" or "branches" that cannot be directly compared.

The antisymmetric property deserves special attention because it captures something profound about hierarchical relationships. When you see that if $aRb$ and $bRa$, then $a = b$, you're seeing mathematics formalize the intuitive idea that if two things are mutually "less than or equal to" each other, they must actually be the same thing. This prevents contradictory relationships and ensures the consistency of your ordering.

Transitivity acts as the "glue" that holds your ordering together, allowing you to chain relationships across multiple steps. When you establish that $a$ relates to $b$ and $b$ relates to $c$, transitivity guarantees that $a$ relates to $c$, creating longer chains of comparison that reveal the deeper structure of your ordering.

## Summary and Key Takeaways

**Partial Order Checklist**: A relation $R$ on set $S$ is a partial order if and only if:
- ✓ Reflexive: $\forall a \in S, aRa$
- ✓ Antisymmetric: $\forall a,b \in S, (aRb \land bRa) \Rightarrow a = b$
- ✓ Transitive: $\forall a,b,c \in S, (aRb \land bRc) \Rightarrow aRc$

**Total Order**: A partial order where every pair of elements is comparable: $\forall a,b \in S, aRb \lor bRa$

**Mental Models**:
- **Partial Order**: A hierarchy with some incomparable elements (like a family tree with distant cousins)
- **Total Order**: A complete linear ranking (like finishing positions in a race)

The progression from equivalence relations to partial orders to total orders shows how mathematics captures increasingly structured relationships, from simple groupings to complex hierarchies to complete rankings.