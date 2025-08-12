## Permutations and Combinations

### Introduction

Many counting problems can be solved by finding the number of ways to arrange a specified number of distinct elements from a set of a particular size. The key distinction is whether the order of these elements matters or not. This lecture covers two fundamental concepts for solving such counting problems: **permutations** (where order matters) and **combinations** (where order doesn't matter).

### Permutations

#### Definition
A **permutation** of a set of distinct objects is an arrangement of these objects where order matters. An **r-permutation** is an ordered arrangement of r elements from a set.

The number of r-permutations of a set with n elements is denoted by $P(n,r)$.

#### Example
Let $S = \{1, 2, 3\}$. 
- The ordered arrangement $(3, 1, 2)$ is a 3-permutation of $S$
- The ordered arrangement $(3, 2)$ is a 2-permutation of $S$
- All 2-permutations of $S$ are: $(1,2)$, $(1,3)$, $(2,1)$, $(2,3)$, $(3,1)$, $(3,2)$
- Therefore, $P(3,2) = 6$

#### Formula for Permutations
For a positive integer $n$ and integer $r$ where $0 \leq r \leq n$:

$$P(n,r) = n \times (n-1) \times (n-2) \times \cdots \times (n-r+1)$$

This can be expressed using factorials as:
$$P(n,r) = \frac{n!}{(n-r)!}$$

#### Proof Using Product Rule
- There are $n$ ways to choose the first element
- There are $(n-1)$ ways to choose the second element  
- There are $(n-2)$ ways to choose the third element
- ...
- There are $(n-(r-1)) = (n-r+1)$ ways to choose the last element

By the product rule: $P(n,r) = n \times (n-1) \times (n-2) \times \cdots \times (n-r+1)$

#### Application Example: Prize Winners
**Problem**: How many possible ways are there of selecting a first prize winner, a second prize winner, and a third prize winner from 50 different people?

**Solution**: We need to find the number of 3-permutations from a set of 50 elements:
$$P(50,3) = 50 \times 49 \times 48 = 117,600$$

# Combinations

## Definition

An **r-combination** of elements from a set is an unordered selection of r elements from the set. An r-combination is simply a subset of the set with r elements.

The number of r-combinations of a set with n distinct elements is denoted by $C(n,r)$ or $\binom{n}{r}$, read as "n choose r."

## Formula for Combinations

$$C(n,r) = \binom{n}{r} = \frac{n!}{(n-r)! \cdot r!}$$

This can also be expressed as:
$$\binom{n}{r} = \frac{P(n,r)}{r!}$$

where $P(n,r)$ is the number of permutations of n objects taken r at a time.

## Key Property

From the definition, it follows that:
$$\binom{n}{r} = \binom{n}{n-r}$$

This symmetry property reflects the fact that choosing r elements to include is equivalent to choosing (n-r) elements to exclude.

## Application Example: Tennis Team Selection

**Problem**: A tennis team has 20 members. Find the number of ways to choose 6 players for an international competition.

**Solution**: Since the order of selection doesn't matter, we need the number of 6-combinations from 20 elements:

$$\binom{20}{6} = \frac{20!}{6! \cdot 14!}$$

We can simplify this by canceling out the common factorial terms:  (**Note the 14! cancels out**)

$$\binom{20}{6} = \frac{20 \times 19 \times 18 \times 17 \times 16 \times 15}{6!}$$

$$= \frac{20 \times 19 \times 18 \times 17 \times 16 \times 15}{6 \times 5 \times 4 \times 3 \times 2 \times 1}$$

Calculating step by step:
- Numerator: $20 \times 19 \times 18 \times 17 \times 16 \times 15 = 27{,}907{,}200$
- Denominator: $6! = 6 \times 5 \times 4 \times 3 \times 2 \times 1 = 720$

Therefore:
$$\binom{20}{6} = \frac{27{,}907{,}200}{720} = 38{,}760$$

**Answer**: There are 38,760 ways to choose 6 players from a team of 20 members.

### Key Differences: Permutations vs Combinations

| Aspect | Permutations | Combinations |
|--------|-------------|--------------|
| **Order** | Matters | Doesn't matter |
| **Formula** | $P(n,r) = \frac{n!}{(n-r)!}$ | $C(n,r) = \frac{n!}{(n-r)! \cdot r!}$ |
| **Relationship** | $P(n,r) = C(n,r) \times r!$ | $C(n,r) = \frac{P(n,r)}{r!}$ |
| **Example** | Selecting president, VP, secretary | Selecting committee members |

### When to Use Each Method

**Use Permutations when:**
- Order/sequence matters
- Different arrangements of the same elements are considered different
- Examples: Rankings, passwords, seating arrangements

**Use Combinations when:**  
- Order doesn't matter
- Different arrangements of the same elements are considered the same
- Examples: Selecting teams, choosing subsets, lottery numbers

### Summary

This lecture introduced two fundamental counting concepts:

1. **Permutations**: Ordered arrangements where the sequence of selection matters
2. **Combinations**: Unordered selections where only the choice of elements matters

Understanding when to apply permutations versus combinations is crucial for solving counting problems correctly. The key question to ask is: "Does the order of selection matter in this problem?"