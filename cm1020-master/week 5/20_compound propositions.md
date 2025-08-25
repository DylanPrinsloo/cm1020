# **Compound propositions** and logical operations:

## **Compound Propositions**

A **compound proposition** is a logical statement formed by combining **two or more simple propositions** using **logical operators**.

---

### Logical Operators Covered:

| Operator         | Symbol | Meaning                | Truth Table Notes                              |
| ---------------- | ------ | ---------------------- | ---------------------------------------------- |
| **Negation**     | ¬p     | “Not p”                | True becomes False, False becomes True         |
| **Conjunction**  | p ∧ q  | “p and q”              | True only if **both** p and q are True         |
| **Disjunction**  | p ∨ q  | “p or q”               | False only if **both** p and q are False       |
| **Exclusive-Or** | p ⊕ q  | “p or q, but not both” | True only if **exactly one** of p or q is True |

---

## Examples Explained:

Assume two propositions:

* **p**: *n is an even number*
* **q**: *n is less than 10*

### **1.** "n is an even number and less than 10"

**→ p ∧ q**

| p | q | p ∧ q |
| - | - | ----- |
| F | F | F     |
| F | T | F     |
| T | F | F     |
| T | T | T     |

---

### **2.** "n is either an even number or less than 10"

**→ p ∨ q**

| p | q | p ∨ q |
| - | - | ----- |
| F | F | F     |
| F | T | T     |
| T | F | T     |
| T | T | T     |

---

### **3.** "n is either even or less than 10, but not both"

**→ p ⊕ q** (exclusive-or)

| p | q | p ⊕ q |
| - | - | ----- |
| F | F | F     |
| F | T | T     |
| T | F | T     |
| T | T | F     |

---

## Operator Precedence

Just like in math, **logic operators have an order** to avoid ambiguity:

1. **Negation (¬)** – Highest priority
2. **Conjunction (∧)**
3. **Disjunction (∨)**
4. **Exclusive-Or (⊕)** – Usually same as disjunction
5. **Implication (→)** and **Biconditional (↔)** – Lower precedence

**Example:**

* Expression: `¬ p ∨ q ∧ r`
* Precedence: compute `¬ p`, then `q ∧ r`, then the final `∨`

---

## Summary

* **Negation** reverses truth.
* **Conjunction** is only true if both are true.
* **Disjunction** is true if at least one is true.
* **Exclusive-or** is true if one is true, but not both.
* Use **truth tables** to visualize all possible combinations.
* Use **operator precedence** to avoid ambiguity in compound statements.
