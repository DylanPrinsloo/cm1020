# De Morgan's Laws for Quantifiers

## Introduction

In predicate logic, De Morgan's laws allow us to understand how negation interacts with quantifiers. These laws provide formal rules for handling the negation of quantified expressions.

## Intuition Behind De Morgan's Laws

Let's consider two examples to understand the intuition:

1. Let S denote: "All the university's computers are connected to the network"
2. Let P denote: "There is at least one computer in the university operating on Linux"

Intuitively:
- The negation of S can be verified if there is at least one computer not connected to the network
- The negation of P can be verified if all university computers are not operating on Linux

## Formal Expression of De Morgan's Laws

Let P be a predicate over the variable x:

1. **Negating Universal Quantifier**:
   - ¬(∀x P(x)) ≡ ∃x ¬P(x)
   - "The negation of 'for all x, P(x)' is equivalent to 'there exists an x for which not P(x)'"

2. **Negating Existential Quantifier**:
   - ¬(∃x P(x)) ≡ ∀x ¬P(x)
   - "The negation of 'there exists an x for which P(x)' is equivalent to 'for every x, not P(x)'"

## Examples of Applying De Morgan's Laws

### Example 1:
Let S be the statement: "Every student of Computer Science has taken a course in Neural Networks"

- Formalization: ∀x P(x)
  - Universe: Students in Computer Science
  - P(x): "x has taken a course in Neural Networks"

- Negation of S: "It is not the case that every student of Computer Science has taken a course in Neural Networks"
  - ¬(∀x P(x)) ≡ ∃x ¬P(x)
  - Meaning: "There is at least one student who has not taken a course in Neural Networks"

### Example 2:
Let R denote: "There is a student of Computer Science who didn't take a course in Machine Learning"

- Formalization: ∃x Q(x)
  - Universe: Students in Computer Science
  - Q(x): "x didn't take a course in Machine Learning"

- Negation of R: "It is not the case that there is a student of Computer Science who didn't take a course in Machine Learning"
  - ¬(∃x Q(x)) ≡ ∀x ¬Q(x)
  - Meaning: "Every student in Computer Science has taken a course in Machine Learning"

## Negating Nested Quantifiers

For nested quantifiers, we apply De Morgan's laws successively from left to right.

For example, let P(x,y,z) denote a propositional function of variables x, y, and z:

The negation of ∀x ∃y ∀z P(x,y,z) is:
- ¬(∀x ∃y ∀z P(x,y,z)) ≡ ∃x ¬(∃y ∀z P(x,y,z)) ≡ ∃x ∀y ¬(∀z P(x,y,z)) ≡ ∃x ∀y ∃z ¬P(x,y,z)

The pattern is to move the negation through all quantifiers, replacing each ∀ with ∃ and vice versa.

## Summary

In this lecture, we examined how De Morgan's laws apply to predicate logic. We explored the intuition behind these laws, gave their formal expressions, and demonstrated how they can be used when negating both simple and nested quantifiers.