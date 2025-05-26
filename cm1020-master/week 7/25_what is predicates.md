# What Are Predicates?

## Introduction

Predicate logic addresses the limitations of propositional logic by enabling us to work with statements whose truth values depend on variables. Let's explore how predicates form the foundation of this more powerful logical system.

## Definition of Predicates

Predicates are generalizations of propositions. They are functions that return a true or false value depending on their variables. The key characteristics of predicates are:

- They become propositions when their variables are assigned actual values
- They represent properties that subjects (variables) can have
- They can be formalized as P(x), where P is the predicate and x is the variable

## Single-Parameter Predicates

Consider the statement "x² = 4". This statement contains two parts:
- The variable x (subject of the statement)
- The predicate "squared is equal to four" (property that the subject can have)

This can be formalized as P(x), where P is the predicate "squared is equal to four" and x is the variable. P is a propositional function that becomes a proposition with a truth value once x is assigned a value:

- P(2) is true
- P(3) is false

## Multi-Parameter Predicates

Predicates can have multiple parameters. For example:

### Two-Parameter Predicate Example
Let P(x,y) denote "x² is greater than y"

- P(-2,3) is equivalent to "4 is greater than 3" (true)
- P(2,4) is equivalent to "4 is greater than 4" (false)

### Three-Parameter Predicate Example
Let Q(x,y,z) denote "x + y is less than z"

- Q(2,4,5) is equivalent to "6 is less than 5" (false)
- Q(1,3,7) is equivalent to "4 is less than 7" (true)
- Q(1,3,z) is "4 is less than z" (not a proposition until z is given a value)

## Logical Operations with Predicates

The logical operations from propositional logic can be applied to predicates:

If P(x) denotes "x² is less than 16", then:

- P(1) ∨ P(-5) is equivalent to "1 is less than 16" OR "25 is less than 16"
  - This is equivalent to true ∨ false, which is true

- P(1) ∧ P(-5) is equivalent to "1 is less than 16" AND "25 is less than 16"
  - This is equivalent to true ∧ false, which is false

- P(3) ∧ P(y) is not a proposition, as y has no assigned value
  - It becomes a proposition only when y is assigned a value

## Summary

Predicate logic extends propositional logic by allowing us to work with variables. Predicates are functions that return truth values and become propositions when their variables are assigned specific values. This approach allows us to express more complex logical relationships and apply the same logical operations we learned in propositional logic.