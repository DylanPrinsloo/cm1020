### **Propositional Logic**

* **Atomic proposition**: a simple statement with a truth value.
* **Connectives**:

  * ¬P = NOT P
  * P ∧ Q = P AND Q
  * P ∨ Q = P OR Q (inclusive unless stated otherwise)
  * P → Q = If P then Q
  * P ↔ Q = P if and only if Q
* **Tools**:

  * Truth tables for evaluating compound statements.
  * Logical equivalences (e.g. De Morgan’s Laws: ¬(P ∧ Q) ≡ ¬P ∨ ¬Q).
* **Application in CS**: digital circuits, conditionals in code, reasoning about algorithms.

---

### **Predicate Logic**

* Extends propositional logic with **variables** and **quantifiers**.
* **Predicates**: P(x), e.g. “x is prime”.
* **Quantifiers**:

  * ∀x P(x): “for all x, P(x) is true.”
  * ∃x P(x): “there exists an x such that P(x) is true.”
* **Negating quantifiers**:

  * ¬∀x P(x) ≡ ∃x ¬P(x)
  * ¬∃x P(x) ≡ ∀x ¬P(x)
* **Application in CS**: databases (SQL queries = predicates + quantifiers), formal specifications, proving correctness.

---

### **Set Theory**

* A set = collection of **distinct elements**.
* **Notation**:

  * x ∈ A (x is an element of A)
  * A ⊆ B (A is subset of B)
  * A ∪ B (union), A ∩ B (intersection), A \ B (difference)
  * |A| = cardinality (size of set A)
* **Special sets**: ∅, ℕ, ℤ, ℚ, ℝ.
* **Relations & Functions**:

  * A relation is a subset of A × B.
  * A function f: A → B assigns each a ∈ A exactly one b ∈ B.
* **Application in CS**: data structures (hash sets, maps), relational databases, defining domains of algorithms.

---

👉 Quick mental hook:

* **Propositional** = whole statements.
* **Predicate** = statements about objects.
* **Sets** = the objects themselves.

