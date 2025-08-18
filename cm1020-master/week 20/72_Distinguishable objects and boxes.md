# Balls and Boxes: A Framework for Counting

### Introduction

Many combinatorial problems can be rephrased as problems of **placing objects into boxes**. By carefully classifying whether the objects and boxes are **distinguishable or indistinguishable**, and whether placement is done **with or without exclusion** (i.e., at most one per box vs. no limit), we obtain a systematic framework for solving a wide range of counting problems.

Key distinctions:

* **Distinguishable objects**: Each object is labeled uniquely (e.g., balls numbered 1 through $k$).
* **Indistinguishable objects**: Objects are identical, no labels (e.g., plain identical balls).
* **Distinguishable boxes**: Each box is labeled uniquely (e.g., boxes numbered 1 through $n$).
* **Indistinguishable boxes**: Boxes are identical, no labels.
* **With exclusion**: No box can contain more than one object.
* **Without exclusion**: A box can contain any number of objects.

This “balls and boxes” framework will now be explored case by case.

---

## Case 1: Distinguishable Balls → Distinguishable Boxes (With Exclusion)

#### Problem Statement

Distribute $k$ balls, each uniquely labeled, into $n$ labeled boxes, with the restriction that **no box may contain more than one ball**.

#### Interpretation

This is equivalent to choosing an ordered arrangement of $k$ boxes from $n$. Each ball chooses a unique box.

#### Formula

The number of such distributions equals the number of **permutations** of $k$ objects from $n$:

$$
P(n,k) = \frac{n!}{(n-k)!}
$$

#### Example

* $n = 5$ boxes, $k = 3$ balls
* Number of distributions = $\frac{5!}{(5-3)!} = \frac{5!}{2!} = 60$

---

## Case 2: Distinguishable Balls → Distinguishable Boxes (Without Exclusion)

#### Problem Statement

Distribute $k$ labeled balls into $n$ labeled boxes, with **no restriction** on how many balls may be placed in a box.

#### Interpretation

Each of the $k$ balls independently chooses one of the $n$ boxes. Since balls are labeled, the sequence of choices matters.

#### Formula

This is equivalent to **permutations with repetition**:

$$
n^k
$$

#### Example

* $n = 3$ boxes, $k = 4$ balls
* Each ball has 3 choices → total distributions = $3^4 = 81$

---

## Case 3: Indistinguishable Balls → Distinguishable Boxes (With Exclusion)

#### Problem Statement

Distribute $k$ identical balls into $n$ labeled boxes, with the restriction that no box may contain more than one ball.

#### Interpretation

This reduces to simply choosing which $k$ boxes will contain a ball, since the balls themselves are indistinguishable.

#### Formula

The number of such distributions equals the number of **combinations**:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

#### Example

* $n = 6$ boxes, $k = 2$ balls
* Number of distributions = $\binom{6}{2} = 15$

---

## Case 4: Indistinguishable Balls → Distinguishable Boxes (Without Exclusion)

#### Problem Statement

Distribute $k$ identical balls into $n$ labeled boxes, with no restriction on the number of balls per box.

#### Interpretation

This is equivalent to a **stars and bars** problem: dividing $k$ identical balls among $n$ labeled bins.

#### Formula

$$
\binom{n+k-1}{k} = \frac{(n+k-1)!}{k!(n-1)!}
$$

#### Example

**Problem**: How many ways are there to place 8 indistinguishable balls into 6 labeled boxes?
**Solution**:

$$
\binom{6+8-1}{8} = \binom{13}{8} = 1287
$$

---

## Complete Summary Table

| Objects               | Boxes               | Exclusion?        | Formula             |
| --------------------- | ------------------- | ----------------- | ------------------- |
| **Distinguishable**   | **Distinguishable** | With exclusion    | $\frac{n!}{(n-k)!}$ |
| **Distinguishable**   | **Distinguishable** | Without exclusion | $n^k$               |
| **Indistinguishable** | **Distinguishable** | With exclusion    | $\binom{n}{k}$      |
| **Indistinguishable** | **Distinguishable** | Without exclusion | $\binom{n+k-1}{k}$  |

---

## Applications in Computer Science

1. **Memory Allocation**: Assigning processes (balls) to processors (boxes).
2. **Database Design**: Distributing identical data blocks across storage servers.
3. **Hashing**: Keys as balls, slots as boxes; collisions depend on with/without exclusion.
4. **Load Balancing**: Modeling identical tasks into labeled machines.

---

## Key Insights

1. **Distinguishability matters**: Labeled vs. unlabeled objects/boxes changes the model.
2. **Exclusion vs. non-exclusion**: Determines whether permutations or combinations apply.
3. **Stars and Bars**: Fundamental technique for distributing indistinguishable objects.
4. **Framework thinking**: Many seemingly different problems reduce to “balls in boxes.”

---

## Summary

In this lecture, we developed the **balls and boxes framework** for counting problems. By classifying whether objects and boxes are distinguishable and whether placement is with or without exclusion, we derived four fundamental formulas:

1. $P(n,k) = \frac{n!}{(n-k)!}$
2. $n^k$
3. $\binom{n}{k}$
4. $\binom{n+k-1}{k}$
