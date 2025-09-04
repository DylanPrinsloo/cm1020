This file is intended for revision purposes only. 
Made by : Dylan
---

### **Propositional Logic**

**Propositional Variables & Connectives**
* Variables: $p, q, r$ (represent propositions)
* Connectives: $\neg$ (not), $\wedge$ (and), $\vee$ (or), $\rightarrow$ (implies), $\leftrightarrow$ (if and only if)

**Propositions**
* Declarative statements that are either true or false
* "The sky is blue" (proposition)
* "What time is it?" (not a proposition)

**Truth Values**
* True ($T$ or $1$)
* False ($F$ or $0$)
* Every proposition has exactly one truth value

**Logical Operations**
* Negation: $\neg p$ (opposite of $p$)
* Conjunction: $p \wedge q$ (both $p$ and $q$ true)
* Disjunction: $p \vee q$ (at least one true)
* Implication: $p \rightarrow q$ (if $p$ then $q$)
* Biconditional: $p \leftrightarrow q$ ($p$ if and only if $q$)

**Logical Equivalence**
* Two propositions with same truth values
* $p \equiv q$ ($p$ is logically equivalent to $q$)
* De Morgan's Laws: $\neg(p \wedge q) \equiv \neg p \vee \neg q$

**Inference Rules**
* Modus Ponens: $p \rightarrow q, p \therefore q$
* Modus Tollens: $p \rightarrow q, \neg q \therefore \neg p$
* Disjunctive Syllogism: $p \vee q, \neg p \therefore q$
* Hypothetical Syllogism: $p \rightarrow q, q \rightarrow r \therefore p \rightarrow r$

---

### **Predicate Logic**

**First Order Logic**
* Uses variables and predicates
* $P(x)$ = predicate $P$ applied to variable $x$
* Returns propositions when variables assigned

**Quantifiers**
* Universal: $\forall x P(x)$ (for all $x$, $P(x)$ is true)
* Existential: $\exists x P(x)$ (there exists $x$ such that $P(x)$)
* Uniqueness: $\exists! x P(x)$ (there exists exactly one $x$)

**Universe of Discourse**
* Universal set of all possible values for variables
* Defines scope of quantifiers
* Example: $\mathbb{N}$ (natural numbers), $\mathbb{R}$ (real numbers)

**Logic Connections**
* Same as propositional: $\neg, \wedge, \vee, \rightarrow, \leftrightarrow$
* Applied to predicates and quantified statements

**Logic Inference**
* Universal Instantiation: $\forall x P(x) \therefore P(a)$
* Existential Instantiation: $\exists x P(x) \therefore P(c)$ for some $c$
* Universal Generalization: $P(a)$ for arbitrary $a \therefore \forall x P(x)$

**Nested Quantifiers**
* Multiple quantifiers in same statement
* $\forall x \exists y P(x,y)$ vs $\exists y \forall x P(x,y)$
* Order matters!

---

### **Mathematical Proofs and Recursion**

**Direct Proof**
* Assume premises, use logic to reach conclusion
* If $P$ then $Q$: assume $P$, prove $Q$

**Proof by Contradiction**
* Assume negation of what you want to prove
* Show this leads to contradiction

**Proof by Contrapositive**
* To prove $P \rightarrow Q$, prove $\neg Q \rightarrow \neg P$

**Mathematical Induction**
* Base case: prove $P(1)$ true
* Inductive step: assume $P(k)$, prove $P(k+1)$
* Conclude $P(n)$ true for all $n \geq 1$

**Recursion**
* Base case: simplest instance
* Recursive case: reduce to smaller problem

---

### **Set Theory**

**Cardinality**
* Number of elements in a set
* $|A|$ = cardinality of set $A$
* $|\emptyset| = 0$ (empty set)

**Power Sets**
* Set of all subsets of a set
* $\mathcal{P}(A)$ = power set of $A$
* If $|A| = n$, then $|\mathcal{P}(A)| = 2^n$

**Set Operations**
* Union: $A \cup B$ (all elements in $A$ or $B$)
* Intersection: $A \cap B$ (elements in both $A$ and $B$)
* Difference: $A \setminus B$ (elements in $A$ but not $B$)
* Complement: $A'$ (elements not in $A$)

**Set-Builder Notation**
* $\{x \mid \text{condition}\}$
* $\{x \in \mathbb{N} \mid x < 5\} = \{1, 2, 3, 4\}$
* Describes sets by properties

---

### **Functions and Relations**

**Functions**
* Map elements from domain to codomain
* Injective (one-to-one): each output has unique input
* Surjective (onto): every output is mapped to
* Bijective: both injective and surjective

**Inverse Functions**
* $f^{-1}$: reverses mapping of $f$
* Only exists for bijective functions

**Relations**
* Reflexive: $aRa$ for all $a$
* Symmetric: $aRb$ implies $bRa$
* Antisymmetric: $aRb$ and $bRa$ implies $a = b$
* Transitive: $aRb$ and $bRc$ implies $aRc$

**Equivalence Relations**
* Reflexive, symmetric, and transitive
* Partitions set into equivalence classes

**Partial Order**
* Reflexive, antisymmetric, and transitive

---

### **Combinations and Permutations**

**Permutations**
* Order matters
* $P(n,r) = \frac{n!}{(n-r)!}$
* Arrangements of $r$ objects from $n$

**Combinations**
* Order doesn't matter
* $C(n,r) = \binom{n}{r} = \frac{n!}{r!(n-r)!}$
* Selections of $r$ objects from $n$

---

### **Graph Theory**

**Basic Concepts**
* Vertices (nodes) and edges
* Directed vs undirected graphs
* Weighted graphs have edge weights

**Euler Paths and Cycles**
* Euler path: visits every edge exactly once
* Euler cycle: Euler path that returns to start
* Exists if graph has $0$ or $2$ odd-degree vertices

**Hamiltonian Paths**
* Visits every vertex exactly once
* NP-complete problem

**Degree Sequences**
* List of vertex degrees in a graph
* Sum must be even (handshaking lemma)
* Graphical sequence: can realize as simple graph
* Non-increasing order: $d_1 \geq d_2 \geq \ldots \geq d_n$

**Complexity Classes**
* P problems: polynomial time solvable
* NP problems: verifiable in polynomial time
* NP-complete: hardest problems in NP
* EXP problems: exponential

---

### **Boolean Algebra**

**Basic Elements**
* Binary variables ($0, 1$)
* Constants ($0, 1$)
* Operations: AND, OR, NOT

**Logical Gates**
* AND gate: output $1$ if both inputs $1$
* OR gate: output $1$ if at least one input $1$
* NOT gate: inverts input

**Simplification Laws**
* Idempotence: $A \wedge A = A$
* Identity: $A \wedge 1 = A$, $A \vee 0 = A$
* Null: $A \wedge 0 = 0$, $A \vee 1 = 1$
* Complement: $A \wedge \neg A = 0$, $A \vee \neg A = 1$

**Karnaugh Maps**
* Visual method to simplify Boolean expressions
* Group adjacent $1$s to find minimal expressions

---

### **Algorithms**

**Basic Properties**
* Input, output, definiteness, effectiveness, finiteness

**Dijkstra's Algorithm**
* Finds shortest path in weighted graph
* Greedy algorithm using priority queue
* Time complexity: $O((V +E) log V)$