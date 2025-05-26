# Nested Quantifiers in Predicate Logic

## Introduction to Nested Quantifiers

In this lecture, we will explore the properties of nested quantifiers. We'll cover:
- Introduction to nested quantifiers
- Binding variables and logical operators
- [Order of operators](images/logical_operators_for_predicate.png) and precedence of quantifiers

## Using Nested Quantifiers

To express statements with multiple variables, we use nested quantifiers. Let's examine the meaning of some common nested quantifier patterns:

- **∀x ∀y P(x,y)** means that P(x,y) is true for every pair x,y
- **∃x ∃y P(x,y)** means that there is at least one pair x,y for which P(x,y) is true
- **∀x ∃y P(x,y)** means that for every x there is a y for which P(x,y) is true
- **∃x ∀y P(x,y)** means that there is an x for which P(x,y) is true for every y

## [Bound and Free Variables](images/binding_variables.png)

The variables of a predicate can be either bound or free:

- A variable is **bound** if it is within the scope of a quantifier
- A variable is **free** if it is not bound by a quantifier or particular value

For instance, let P be a propositional function, and S the statement ∃x P(x,y). We can say that:
- x is bound (by the existential quantifier)
- y is free (not bound by any quantifier)

## [Logical Operations with Quantified Statements](images/logical_operators_for_predicate.png)

The logical operations introduced in propositional logic (negation, disjunction, conjunction, implication, and equivalence) can also be applied to quantified statements.

### Examples:

If:
- P(x) denotes "x is greater than 3"
- Q(x) denotes "x² is even"

Then:
- ∃x (P(x) ∧ Q(x)) is equivalent to true, because x = 4 satisfies both conditions
- ∀x (P(x) → Q(x)) is equivalent to false, because x = 5 doesn't satisfy this condition

## [Order of Quantifiers](images/order_of_operators.png)

When nested quantifiers are of the same type, the order doesn't matter:

- ∀x ∀y P(x,y) is equivalent to ∀y ∀x P(x,y)
- ∃x ∃y P(x,y) is equivalent to ∃y ∃x P(x,y)

[However, the order does matter if the quantifiers are of different types:](precedence_of_quantifiers.png)

- ∀x ∃y P(x,y) is different from ∃y ∀x P(x,y)

In order to simplify the notation of nested quantifiers, certain conventions in notation are followed.