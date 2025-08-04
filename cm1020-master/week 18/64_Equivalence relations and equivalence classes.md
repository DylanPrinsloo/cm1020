# Equivalence Relations: Complete Study Notes

## Core Definition and Intuition

An **equivalence relation** is a mathematical way to formalize the notion of "sameness" or "equality" between elements of a set. Think of it as a generalized concept of equality that allows us to group elements that share some common property.

### Formal Definition

Let $R$ be a relation on a set $S$. Then $R$ is an **equivalence relation** if and only if $R$ satisfies all three of the following properties:

1. **Reflexive**: For all $a \in S$, we have $aRa$ (every element is related to itself)
2. **Symmetric**: For all $a, b \in S$, if $aRb$ then $bRa$ (the relation works both ways)
3. **Transitive**: For all $a, b, c \in S$, if $aRb$ and $bRc$, then $aRc$ (the relation chains together)

### Why These Three Properties Matter

Think of these properties as the fundamental characteristics that make a relation behave like "equality":

- **Reflexivity** ensures that every element is equivalent to itself, just like $a = a$
- **Symmetry** ensures that if $a$ is equivalent to $b$, then $b$ is equivalent to $a$, just like equality
- **Transitivity** ensures that equivalence is consistent across chains of relationships

## [Example 1: Modular Arithmetic (Equivalence Relation)](images/example_one_of_equivalence_relation.png)

Consider the relation $R$ on $\mathbb{Z}$ where $(a,b) \in R$ if and only if:

$$a \equiv b \pmod{2}$$

This means $a$ and $b$ have the same remainder when divided by 2.

**Verification that this is an equivalence relation:**

- **Reflexive**: For any $a \in \mathbb{Z}$, clearly $a \equiv a \pmod{2}$ since $a - a = 0$ is even
- **Symmetric**: If $a \equiv b \pmod{2}$, then $a - b$ is even, which means $b - a = -(a - b)$ is also even, so $b \equiv a \pmod{2}$
- **Transitive**: If $a \equiv b \pmod{2}$ and $b \equiv c \pmod{2}$, then both $a - b$ and $b - c$ are even, so $(a - b) + (b - c) = a - c$ is even, meaning $a \equiv c \pmod{2}$

This relation partitions the integers into two groups: even numbers and odd numbers.

## [Example 2: Inequality Relation (NOT an Equivalence Relation)](images/example_two_of_not_a_equivalence_relation.png)

Consider the relation $R$ on $\mathbb{Z}$ where $(a,b) \in R$ if and only if $a \leq b$.

**Why this fails to be an equivalence relation:**

- **Reflexive**: ✓ Yes, $a \leq a$ for all $a \in \mathbb{Z}$
- **Symmetric**: ✗ No! Take $a = 2, b = 3$. We have $2 \leq 3$, but $3 \not\leq 2$
- **Transitive**: ✓ Yes, if $a \leq b$ and $b \leq c$, then $a \leq c$

Since symmetry fails, this is not an equivalence relation. This example shows why all three properties are essential.

## [Equivalence Classes: The Heart of the Matter](images/example_of_equivalence_classes.png)

Once we have an equivalence relation, we can use it to partition our set into **equivalence classes**.

### Definition

Let $R$ be an equivalence relation on set $S$. The **equivalence class** of element $a \in S$ is:

$$[a] = \{x \in S : xRa\}$$

The square brackets $[a]$ denote "the equivalence class containing $a$."

### Key Properties of Equivalence Classes

1. **Every element belongs to exactly one equivalence class**
2. **Two equivalence classes are either identical or disjoint**
3. **The union of all equivalence classes equals the original set**

This creates what mathematicians call a **partition** of the set.

## [Worked Example: Modulo 2 Equivalence Classes](images/example_two_of_equivalence_classes.png)

Using our relation $R$ where $a \equiv b \pmod{2}$ on the set $S = \{1, 2, 3, 4\}$:

**Finding the equivalence classes:**

- $[1] = \{x \in S : x \equiv 1 \pmod{2}\} = \{1, 3\}$ (odd numbers)
- $[2] = \{x \in S : x \equiv 2 \pmod{2}\} = \{2, 4\}$ (even numbers)

Notice that $[1] = [3]$ and $[2] = [4]$ because equivalent elements have identical equivalence classes.

## Another Example: Even Difference Relation

Consider $R$ on $\mathbb{Z}$ where $(a,b) \in R$ if and only if $a - b$ is even.

**This relation on $S = \{1, 2, 3, 4, 5\}$ gives us:**

- Equivalence class of odd numbers: $[1] = [3] = [5] = \{1, 3, 5\}$
- Equivalence class of even numbers: $[2] = [4] = \{2, 4\}$

**The relation pairs are:**
$R = \{(1,1), (2,2), (3,3), (4,4), (5,5), (2,4), (4,2), (1,3), (3,1), (1,5), (5,1), (3,5), (5,3)\}$

## Deep Understanding: Why Equivalence Relations Matter

Equivalence relations are fundamental because they allow us to:

1. **Abstract away irrelevant differences**: Focus on what makes elements "the same" for our purposes
2. **Simplify complex sets**: Replace complicated sets with simpler quotient structures
3. **Define consistent operations**: Work with equivalence classes as single entities

Think of equivalence relations as mathematical "equality with flexibility" - they let us decide what aspects of elements we care about and ignore the rest.

## Summary and Key Takeaways

**Definition Checklist**: A relation $R$ on set $S$ is an equivalence relation if and only if:
- ✓ Reflexive: $\forall a \in S, aRa$
- ✓ Symmetric: $\forall a,b \in S, aRb \Rightarrow bRa$  
- ✓ Transitive: $\forall a,b,c \in S, (aRb \land bRc) \Rightarrow aRc$

**Equivalence Classes**: The equivalence class $[a] = \{x \in S : xRa\}$ partitions the set into disjoint subsets where all elements in each subset are equivalent to each other.

**Mental Model**: Think of equivalence relations as sophisticated sorting mechanisms that group elements based on shared essential properties while ignoring irrelevant differences.