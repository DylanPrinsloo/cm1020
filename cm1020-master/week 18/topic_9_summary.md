# Topic 9 Summary

A relation $R$ from a set $A$ to a set $B$ is a subset of the Cartesian product $A \times B$. That is,

$$
R \subseteq A \times B.
$$

If $(a, b) \in R$, we say that **a is related to b** by $R$.

---

## Properties of Relations

* **Reflexive**: Every element is related to itself.

  $$
  \forall a \in A,\, (a, a) \in R
  $$

* **Symmetric**: If an element is related to another, then the second element is related to the first.

  $$
  \forall a, b \in A,\ (a, b) \in R \Rightarrow (b, a) \in R
  $$

* **Anti-symmetric**: If an element is related to another and vice versa, then they must be the same element.

  $$
  \forall a, b \in A,\ (a, b) \in R \land (b, a) \in R \Rightarrow a = b
  $$

* **Transitive**: If an element is related to a second element, which is related to a third element, then the first element is related to the third.

  $$
  \forall a, b, c \in A,\ (a, b) \in R \land (b, c) \in R \Rightarrow (a, c) \in R
  $$

---

## Adjacency Matrix of a Relation

A relation can be defined by its **adjacency matrix**. Reflexivity, symmetry, and anti-symmetry of a relation $R$ can be easily deduced from its corresponding adjacency matrix.

---

## Equivalence Relation

* A relation that is **reflexive, symmetric, and transitive**.
* Partitions the set into **equivalence classes**.

---

## Partial Order

* A relation that is **reflexive, anti-symmetric, and transitive**.
* Provides a way to order elements in a set.

---

## Total Order

* A **partial order** where **every pair of elements is comparable**.
* Also called a **linear order**.

---

# Equivalence Classes

Given an equivalence relation $R$ on a set $A$, the equivalence class of an element $a \in A$, denoted by $[a]$, is:

$$
[a] = \{ x \in A \mid (a, x) \in R \}
$$

Equivalence classes **partition the set** $A$ into disjoint subsets where every element in $A$ belongs to exactly one equivalence class.

---

# Self-Assessment and Study Strategy

As you progress through your course, regularly assess your understanding and capabilities against the learning outcomes. Use the steps below:

### 1. Review the Learning Outcomes

For each topic's learning outcomes, rate your understanding on a scale of 1–5 (1 = very low, 5 = very high).
**Provide a brief explanation** for your rating.

### 2. Identify Areas for Improvement

* Identify any areas where your rating is **below 4**.
* For each area, describe what is challenging or unclear.

### 3. Create an Action Plan

For each knowledge gap:

* Review the course materials and textbooks.
* Seek additional resources.
* Practice problems or exercises.
* Ask for help from your instructor or peers.
* Schedule extra study sessions.
