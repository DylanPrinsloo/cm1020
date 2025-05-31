# [Rules of Inference with Quantifiers](images/rules_of__inference_with_quantification_outlined.png)

## Introduction

In predicate logic, rules of inference are extended to handle quantified statements. These rules allow us to manipulate quantifiers in valid logical arguments.

## Universal Instantiation (UI)

**Rule**: From a universally quantified statement, we can infer any specific instance.

**Formal representation**:
- From ∀x P(x)
- We can derive P(c) for any specific constant c in the universe of discourse

**Example**:
- From "All students study discrete mathematics" (∀x S(x))
- We can infer "John studies discrete mathematics" (S(John))

## Universal Generalization (UG)

**Rule**: If we can prove a property holds for an arbitrary element, we can generalize it to all elements.

**Formal representation**:
- If we can prove P(c) for an arbitrary c (with no specific assumptions about c)
- Then we can derive ∀x P(x)

**Example**:
- If we can prove "If n is an arbitrary integer, then n² ≥ n" without making special assumptions about n
- Then we can conclude "For all integers n, n² ≥ n"

## Existential Instantiation (EI)

**Rule**: From an existential statement, we can infer that there is a specific element with the stated property.

**Formal representation**:
- From ∃x P(x)
- We can introduce a new constant c and infer P(c)
- Note: c must be a new constant not appearing elsewhere in the proof

**Example**:
- From "There exists a student who scored 100% on the exam" (∃x S(x))
- We can infer "Let's call this student c, so S(c) is true"

## Existential Generalization (EG)

**Rule**: From a specific instance of a property, we can infer that there exists an element with that property.

**Formal representation**:
- From P(c) for a specific constant c
- We can derive ∃x P(x)

**Example**:
- From "John speaks French" (S(John))
- We can infer "There exists someone who speaks French" (∃x S(x))

## Combined Rules with Multiple Quantifiers

### Universal Instantiation followed by Existential Generalization

**Example**:
- From "All students take some math course" (∀x ∃y Takes(x,y))
- By UI: "John takes some math course" (∃y Takes(John,y))
- By EI: "John takes math course c" (Takes(John,c))
- By EG with different variable: "There exists a course that John takes" (∃z Takes(John,z))

## Inference Rules with Nested Quantifiers

When dealing with nested quantifiers, we must be careful about the order of applying rules:

1. We typically process the leftmost quantifier first
2. When replacing universally quantified variables, we can use any term
3. When replacing existentially quantified variables, we must use a new constant not appearing elsewhere

**Example**:
From "Everyone has someone they admire" (∀x ∃y Admires(x,y)):
1. Apply UI: "Alice has someone she admires" (∃y Admires(Alice,y))
2. Apply EI: "Alice admires c" (Admires(Alice,c))

## Common Errors to Avoid

1. **Invalid Universal Generalization**: You cannot generalize from specific examples to a universal claim if the example has special properties
2. **Improper Existential Instantiation**: The constant introduced must not appear elsewhere in the proof
3. **Order Confusion**: Be careful with the order of quantifiers, as ∀x ∃y P(x,y) is different from ∃y ∀x P(x,y)

## Summary

Rules of inference for quantifiers allow us to:
- Draw specific conclusions from general statements (UI)
- Make general conclusions from arbitrary examples (UG)
- Identify specific instances from existential statements (EI)
- Make existential claims from specific examples (EG)

These rules, combined with the rules of propositional logic, provide a complete system for constructing valid arguments in predicate logic.