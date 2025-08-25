# **Propositional Logic**:

---

### **What Is Propositional Logic?**

Propositional logic (also called **sentential logic**) is a formal system in which:

* The **basic elements** are **propositions**—statements that are either **true or false**.
* These are treated like **variables** in algebra, but instead of numbers, the values are **truth values**.
* We combine propositions using **logical operators**:

  * **AND (∧)**: Both statements must be true
  * **OR (∨)**: At least one statement is true
  * **NOT (¬)**: Negates a statement (true becomes false)
  * **IMPLIES (→)**: If A is true, then B must be true
  * **IF AND ONLY IF (↔)**: A and B are either both true or both false

Think of it as the **algebra of truth values**.

---

### **Why Is It Important?**

* **Foundation of mathematical reasoning** – It's used to formalize **proofs** and arguments.
* **Old roots** – Goes back to **Aristotle**, who used it to model rational thinking.
* **In computer science**:

  * **Digital circuit design** (logic gates follow propositional rules)
  * **Programming languages** (especially logic programming like **Prolog**)
  * **AI & theorem proving** (automated reasoning, verifying code correctness)

---

### **Examples of Propositional Logic**

Let's define:

* `P`: "It is raining"
* `Q`: "The ground is wet"

Then:

* `P → Q` means: *If it is raining, then the ground is wet*
* `¬P ∨ Q` means: *Either it's not raining, or the ground is wet* (logically equivalent to the above)
* `P ∧ Q` means: *It is raining AND the ground is wet*

---

### **Real Applications**

* **Circuit design**: AND/OR/NOT gates mirror logical operators.
* **AI & reasoning systems**: Used in expert systems to draw conclusions.
* **Software verification**: Prove that code behaves correctly under all conditions.
* **Search problems**: Represent constraints and facts in a structured, logical way.

---

### What Comes Next?

You'll later explore **Predicate Logic**, which extends propositional logic by adding:

* **Variables**, **quantifiers** (`∀`, `∃`)
* Ability to express more complex statements like "All humans are mortal"

