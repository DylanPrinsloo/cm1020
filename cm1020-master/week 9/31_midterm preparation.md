# Midterm Assessment Preparation

## Overview

The midterm assessment is worth **30% of the overall grade** and covers five main topics:

1. Set Theory
2. Functions
3. Propositional Logic
4. Predicate Logic
5. Boolean Algebra

Let's explore what you need to know for each topic:

## 1. Set Theory

### Key Concepts:
- **Set Representation Methods**:
  - Listing method: A = {1, 2, 3}
  - Set builder notation: A = {x | x is a positive integer less than 4}
  - Venn diagrams

```
    ┌────────┐     ┌────────┐
    │        │     │        │
    │   A    │     │    B   │
    │        │     │        │
    └────────┘     └────────┘
```

- **Set Terminology**:
  - Element of a set (∈)
  - Cardinality: |A|
  - Subset: A ⊆ B
  - Powerset: P(A)

- **Set Operations**:
  - Union (A ∪ B)
  - Intersection (A ∩ B)
  - Difference (A - B)
  - Symmetric difference (A △ B)

- **Proof Methods**:
  1. Set laws (commutativity, distributivity, associativity)
  2. Membership tables
  3. Venn diagrams

> **Important**: Do not use examples to prove general statements! Use counterexamples only to disprove statements.

## 2. Functions

### Key Concepts:
- **Function Components**:
  - Domain: input values
  - Co-domain: potential output values
  - Range: actual output values

- **Function Properties**:
  1. **One-to-one (Injective)**:
     - Each input has a unique output
     - If f(a) = f(b), then a = b
     
     ```
     Domain      Range
       o ──────→ •
       o ──────→ •
       o ──────→ •
     ```

  2. **Onto (Surjective)**:
     - Every co-domain element is mapped to
     
     ```
     Domain      Co-domain
       o ──────→ •
       o ┐
         ├────→ •
       o ┘
     ```

  3. **Bijective**:
     - Both one-to-one and onto
     - Has an inverse function

- **Inverse Functions**:
  - Only bijective functions have inverses
  - For f(x), the inverse is f⁻¹(x)

## 3. Propositional Logic

### Key Concepts:
- **Propositions**: Statements that are either true or false

- **Compound Propositions**:
  - Negation (¬p)
  - Conjunction (p ∧ q)
  - Disjunction (p ∨ q)
  - Implication (p → q)
  - Equivalence (p ↔ q)

- **Truth Tables**:

  ```
  p | q | p ∧ q | p ∨ q | p → q | p ↔ q
  --|---|-------|-------|-------|-------
  T | T |   T   |   T   |   T   |   T
  T | F |   F   |   T   |   F   |   F
  F | T |   F   |   T   |   T   |   F
  F | F |   F   |   F   |   T   |   T
  ```

- **Logical Laws**:
  - Idempotent: p ∧ p ≡ p
  - Commutative: p ∧ q ≡ q ∧ p
  - Associative: p ∧ (q ∧ r) ≡ (p ∧ q) ∧ r
  - Distributive: p ∧ (q ∨ r) ≡ (p ∧ q) ∨ (p ∧ r)
  - Identity: p ∧ T ≡ p
  - Domination: p ∨ T ≡ T

- **De Morgan's Laws**:
  - ¬(p ∨ q) ≡ ¬p ∧ ¬q
  - ¬(p ∧ q) ≡ ¬p ∨ ¬q

- **Related Implications**:
  - Converse: q → p
  - Inverse: ¬p → ¬q
  - Contrapositive: ¬q → ¬p

## 4. Predicate Logic

### Key Concepts:
- **Predicates vs. Propositions**:
  - Predicates contain variables and become propositions when values are assigned

- **Quantifiers**:
  - Universal (∀x): "For all x"
  - Existential (∃x): "There exists an x"
  - Uniqueness (∃!x): "There exists exactly one x"

- **Nested Quantifiers**:
  - ∀x ∀y P(x,y): "For all x and all y, P(x,y)"
  - ∃x ∃y P(x,y): "There exists x and y such that P(x,y)"
  - ∀x ∃y P(x,y): "For all x, there exists a y such that P(x,y)"

- **Rules of Inference**:
  - Modus ponens: [(p → q) ∧ p] → q
  - Modus tollens: [(p → q) ∧ ¬q] → ¬p
  - Conjunction: [p ∧ q] → (p ∧ q)
  - Disjunctive syllogism: [(p ∨ q) ∧ ¬p] → q

## 5. Boolean Algebra

### Key Concepts:
- **Boolean Laws**:
  - Apply to simplify Boolean expressions

- **Logic Gates**:
  - AND, OR, NOT, XOR, NAND, NOR

  ```
  AND    OR     NOT    XOR
  
  A─┐    A─┐    A─>o─  A─┐
    │AND    │OR        │XOR
  B─┘    B─┘         B─┘
  ```

- **Converting Between**:
  - Boolean expressions to logic circuits
  - Logic circuits to Boolean expressions

- **Karnaugh Maps**:
  - Visual method to simplify Boolean expressions

  ```
  AB\CD  00  01  11  10
     00   1   1   0   0
     01   1   1   0   0
     11   0   0   0   0
     10   0   0   0   0
  ```

## Summary

To prepare effectively:
- Understand all core concepts for each topic
- Practice applying laws and rules
- Work through proofs and simplifications
- Know how to construct valid arguments
- Use proper proof techniques (avoid using examples to prove general statements)

Good luck with your midterm assessment!