# **Truth tables** and **truth sets**:

## **1. What is a Truth Table?**

A **truth table** is a table that shows **all possible truth values** of a compound proposition based on the **truth values of its components**.

* If you have:

  * 1 variable → 2 rows (`True`, `False`)
  * 2 variables → 4 rows (`2^2`)
  * 3 variables → 8 rows (`2^3`)
  * ...and so on.

Each **row** represents one possible **combination of truth values** for the variables.

---

### Example: Two Variables (`p`, `q`)

| p     | q     |
| ----- | ----- |
| False | False |
| False | True  |
| True  | False |
| True  | True  |

---

### How to Construct a Truth Table (for n variables)

If you have **3 variables** (`p`, `q`, `r`), you need `2^3 = 8` rows. Here's how the pattern works:

| p     | q     | r     |
| ----- | ----- | ----- |
| False | False | False |
| False | False | True  |
| False | True  | False |
| False | True  | True  |
| True  | False | False |
| True  | False | True  |
| True  | True  | False |
| True  | True  | True  |

* **p** alternates every 4 values.
* **q** alternates every 2 values.
* **r** alternates every 1 value.

---

## **2. What is a Truth Set?**

A **truth set** is the set of all elements in a given set `S` for which a **proposition is true**.

We often denote the **truth set of a proposition `p`** as **capital `P`**.

---

### Example:

Let **S = {1, 2, 3, ..., 10}**

Define two propositions for each element `n` in `S`:

* **p(n)**: "`n` is even"
* **q(n)**: "`n` is odd"

Then:

* **Truth set of `p` (denoted `P`)** = `{2, 4, 6, 8, 10}`
* **Truth set of `q` (denoted `Q`)** = `{1, 3, 5, 7, 9}`

This simply groups elements where the proposition evaluates to **True**.

---

## Summary

| Concept     | Meaning                                                                 |
| ----------- | ----------------------------------------------------------------------- |
| Truth Table | A table listing all combinations of truth values for logical variables. |
| Truth Set   | A subset of a domain where a given proposition holds true.              |
