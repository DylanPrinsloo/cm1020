# 1. Introduction

A set is a fundamental concept in mathematics and computer science. It’s a collection of distinct objects, considered as an object in its own right. Sets are used to group related items together and to perform operations on these groups.

---

# 2. Definition of a Set

**Definition 1:** A set is a collection of objects. The objects in a set are called its **elements** or **members**. The elements in a set can be any types of objects, including other sets! The members of a set do not even have to be of the same type.

> Example: A set can consist of numbers and names.

**Definition 2:** A set is an **unordered collection** of **distinct** elements.

> Example: The set of primary colours can be written as `{red, blue, yellow}`.

---

# 3. Notation

- Sets are usually denoted by **capital letters**.
- Elements are listed within **curly braces**.

> Example:  
> Set `A` containing elements 1, 2, and 3 is written as:  
> `A = {1, 2, 3}`

---

## 3.1 Element or Member of a Set (`∈`)

The symbol `∈` denotes **membership** or an **element**

If `a` is an element of a set `A`, we write:  
`a ∈ A`

### Example:

Let `A = {1, 2, 3}`

- `1 ∈ A` means 1 is an element of A  
- `2 ∈ A` means 2 is an element of A  
- `3 ∈ A` means 3 is an element of A

If an object is **not** a member of a set, we use `∉`.

> Example:  
> `4 ∉ A` because 4 is not in the set `{1, 2, 3}`

---

## 3.2 Special Sets of Numbers

- **ℕ =** the set of natural numbers (positive integers)  
- **ℤ =** the set of integers  
- **ℚ =** the set of rational numbers  
- **ℝ =** the set of real numbers  

---

## 3.3 Empty Set (`∅`)

The **empty set** (or null set) is the set that contains **no elements**.

**Definition 3:**  
The empty set is denoted by:  
- `∅`  
- `{}`

> In mathematical notation:  
> `∅ = {}`

---

## 3.4 Cardinality of a Set ( `|A|` )

The **cardinality** of a set is the number of elements in the set.  
It is denoted by `|A|`.

**Definition 4:**  
For a set `A`, `|A|` is the number of **distinct** elements in `A`.

### Examples:

- `A = {1, 2, 3, 4}` → `|A| = 4`  
- `B = {a, b, c}` → `|B| = 3`  
- `∅` (empty set) → `|∅| = 0`

---

## 3.5 Finite and Infinite Sets

- **Finite set:** A set with a **limited** number of elements.  
  > Example: `{2, 4, 6}`

- **Infinite set:** A set with an **unlimited** number of elements.  
  > Example: `ℕ = {1, 2, 3, …}`

---

## 3.6 Exercise

Using set notation, list all the elements contained in each of the following sets:

1. `A =` the set of positive integers less than 8  
2. `B =` the set of even positive integers less than or equal to 10  
3. `C =` the set of natural numbers

---

## 3.7 Solution

1. `A = {1, 2, 3, 4, 5, 6, 7}`  
2. `B = {2, 4, 6, 8, 10}`  
3. `C = ℕ = {1, 2, 3, 4, …}`

---

# 4. Subset of a Set

A subset is another fundamental concept in set theory that describes a relationship between sets.

## 4.1 Definition of a Subset ( `⊆` )

**Definition 5:** A set A is a **subset** of set B if **every** element of A is also an element of B. We denote this as:

`A ⊆ B`

If A is a subset of B, we can also say that B is a **superset** of A.

### Examples:

- If `A = {1, 2}` and `B = {1, 2, 3, 4}`, then `A ⊆ B`
- If `A = {a, b, c}` and `B = {a, b, c}`, then `A ⊆ B` (a set is always a subset of itself)
- The empty set `∅` is a subset of every set

---

## 4.2 Proper Subset

**Definition 6:** A set A is a **proper subset** of B if A is a subset of B **and** A ≠ B (there is at least one element in B that is not in A). We denote this as:

`A ⊂ B`

### Examples:

- If `A = {1, 2}` and `B = {1, 2, 3, 4}`, then `A ⊂ B` (proper subset)
- If `A = {a, b, c}` and `B = {a, b, c}`, then `A ⊆ B` but A is NOT a proper subset of B
- If `A = ∅` and `B = {1, 2, 3}`, then `A ⊂ B` (proper subset)

---

## 4.3 Properties of Subsets

1. Every set is a subset of itself: `A ⊆ A`
2. The empty set is a subset of every set: `∅ ⊆ A`
3. If `A ⊆ B` and `B ⊆ C`, then `A ⊆ C` (transitivity)
4. For a finite set with n elements, the number of possible subsets is 2^n

---

## 4.4 Exercise

For the set `X = {a, b, c}`:

1. List all possible subsets of X
2. Identify which of these subsets are proper subsets
3. Calculate the total number of subsets using the formula

---

## 4.5 Solution

1. All subsets of `X = {a, b, c}`:
   - `∅`
   - `{a}`
   - `{b}`
   - `{c}`
   - `{a, b}`
   - `{a, c}`
   - `{b, c}`
   - `{a, b, c}`

2. Proper subsets of X:
   - `∅`
   - `{a}`
   - `{b}`
   - `{c}`
   - `{a, b}`
   - `{a, c}`
   - `{b, c}`
   
   Note: `{a, b, c}` is NOT a proper subset of X since it equals X.

3. For a set with n = 3 elements, the number of possible subsets is 2^3 = 8, which matches our list.

---

# 5. Summary

This way of representing sets is called the **listing method**.  
In future lessons, we will explore:
- More examples of the listing method
- Other representation methods like **set builder notation**
- How sets are represented using **Venn diagrams**
