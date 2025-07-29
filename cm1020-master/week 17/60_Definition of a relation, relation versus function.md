# Mathematical Relations 

## Informal Definition

A **relation** is a connection or association between elements of two sets, or within a single set. We typically denote a relation by the letter $R$.

Let $A$ and $B$ be two sets. A relation $R$ from $A$ to $B$ is a rule that associates elements of $A$ with elements of $B$. If $x \in A$ and $y \in B$, we write $xRy$ to indicate that $x$ is related to $y$ via $R$.

### [Example](images/example_of_relation_matrix.png)

Let $A$ be the set of students:
$$A = \{\text{Sofia}, \text{Samir}, \text{Sarah}\}$$

Let $B$ be the set of courses:
$$B = \{\text{Mathematics}, \text{Java}, \text{Databases}, \text{Art}\}$$

Define $R$ as "is enrolled in". Then, for instance:
- $(\text{Sofia}, \text{Mathematics}) \in R$
- $(\text{Samir}, \text{Databases}) \in R$
- $(\text{Sarah}, \text{Art}) \in R$

A relation can also be defined within a single set. For example, "is a son of" is a relation on the set of people.

## Cartesian Product

The **Cartesian product** of two sets $A$ and $B$, denoted $A \times B$, is the set of all ordered pairs:
$$A \times B = \{(x, y) \mid x \in A, y \in B\}$$

### Example

If $A = \{a_1, a_2\}$ and $B = \{b_1, b_2, b_3\}$, then:
$$A \times B = \{(a_1, b_1), (a_1, b_2), (a_1, b_3), (a_2, b_1), (a_2, b_2), (a_2, b_3)\}$$

## Formal Definition of a Relation

A **binary relation** from $A$ to $B$ is any subset $R \subseteq A \times B$.

If $(x, y) \in R$, we say $x$ is related to $y$ by $R$.

### Example

Let $A = \{a, b, c\}$, $B = \{1, 2, 3\}$, and $R = \{(a, 1), (b, 2), (c, 3)\}$.

Here, $a$ is related to $1$, $b$ to $2$, and $c$ to $3$.

When $A = B$, $R$ is called a **relation on $A$**, i.e., $R \subseteq A \times A$.

### Example

Let $A = \{1, 2, 3, 4\}$, and define $R$ as "strictly less than":
$$R = \{(x, y) \mid x, y \in A, x < y\}$$

So:
$$R = \{(1,2), (1,3), (1,4), (2,3), (2,4), (3,4)\}$$


